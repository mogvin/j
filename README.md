<xml xmlns="https://developers.google.com/blockly/xml" is_dbot="true" collection="false">
  <variables>
    <variable id="u]@6qd1s}n-P%#SW23iZ">sma_mid</variable>
    <variable id="P${QsG.49i3t/T2Y{ORI">Max Loss Amount</variable>
    <variable id="W85mq?KQPPq=M}Gbowq,">confirm_buy</variable>
    <variable id="lb:;T7(!b|F%_^%##%yn">ema_high</variable>
    <variable id="_^K%$ZT3iAJ0r,=Y)t{e">Expected Profit</variable>
    <variable id="Cr`aM/i9kt_5gWTJdeop">Initial Amount</variable>
    <variable id="f5RncE:Nv!r(gN/kx3Ux">confirm_sell</variable>
    <variable id="x4#5JPs2*L*8h3AbMKjp">bb_mid</variable>
    <variable id="J_sO@e2LThC4)euuGaIn">Win Amount</variable>
    <variable id="rSWvU+{*:EmViRi~y6(W">final_buy</variable>
    <variable id=".IG]LH|qsDGx+7{U-_cu">bb_low</variable>
    <variable id="?6{q@1dMn1rUO}Wdpo%a">final_sell</variable>
    <variable id="ficbIddKcG0H,-jqM$7X">ema_mid</variable>
    <variable id="I)3XQMar#(1p;_oOC!KS">text1</variable>
    <variable id="hawGi,Q;JJ/3,_PGzul[">text2</variable>
    <variable id="loET/e:aUs+;odJPKJSq">text3</variable>
    <variable id="t@%I.Ll]DNl^^rVCfI#R">ema_low</variable>
    <variable id="P);w$.oDv0edq+xZr8^q">RSI</variable>
    <variable id="5t%R8/wO^;qaB|m{{J9[">text4</variable>
    <variable id="(S/imNt40Dig^U{0v.[:">text</variable>
    <variable id="yrsK]*nMA`[.ILEFWbFa">text_1</variable>
    <variable id="1sJ}oeqKGJuzhc,+sSsL">text_2</variable>
    <variable id="5bJ`h_VFI5+1BF3[iLa*">bb_high</variable>
    <variable id="{O*2nA--BG.dq#ykJF:[">text_4</variable>
    <variable id="U_|ZtI3=Zjv=JdeDgwf2">text_3</variable>
  </variables>
  <block type="trade_definition" id="MD1rMv.?jp:g8S#*5K2a" deletable="false" x="0" y="0">
    <statement name="TRADE_OPTIONS">
      <block type="trade_definition_market" id="QuGh~Z5S~o$wRoy~_EZ[" deletable="false" movable="false">
        <field name="MARKET_LIST">synthetic_index</field>
        <field name="SUBMARKET_LIST">random_index</field>
        <field name="SYMBOL_LIST">R_100</field>
        <next>
          <block type="trade_definition_tradetype" id="e_u(+RD.qnRI*lEn}y5F" deletable="false" movable="false">
            <field name="TRADETYPECAT_LIST">callput</field>
            <field name="TRADETYPE_LIST">callput</field>
            <next>
              <block type="trade_definition_contracttype" id="IuXXF$x3;$gZRlVz5kce" deletable="false" movable="false">
                <field name="TYPE_LIST">both</field>
                <next>
                  <block type="trade_definition_candleinterval" id="Y^S0qPM!]EH]M1@!C)[o" deletable="false" movable="false">
                    <field name="CANDLEINTERVAL_LIST">60</field>
                    <next>
                      <block type="trade_definition_restartbuysell" id="/]Y_~*obUcGE{+T?~U$_" deletable="false" movable="false">
                        <field name="TIME_MACHINE_ENABLED">FALSE</field>
                        <next>
                          <block type="trade_definition_restartonerror" id="z(Z$SU?Y7GMb5W9M@f,+" deletable="false" movable="false">
                            <field name="RESTARTONERROR">TRUE</field>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </next>
      </block>
    </statement>
    <statement name="INITIALIZATION">
      <block type="variables_set" id="t;B$gCtQQ=3{Y99Y]*~B">
        <field name="VAR" id="P${QsG.49i3t/T2Y{ORI">Max Loss Amount</field>
        <value name="VALUE">
          <block type="math_number" id="~9fG+Qj#d5A8VO6A1NfN">
            <field name="NUM">50</field>
          </block>
        </value>
        <next>
          <block type="variables_set" id="l@f,K{~Jh,^CQkeaD[[a">
            <field name="VAR" id="_^K%$ZT3iAJ0r,=Y)t{e">Expected Profit</field>
            <value name="VALUE">
              <block type="math_number" id="auqX8%F4bckNoK43%Mq{">
                <field name="NUM">5</field>
              </block>
            </value>
            <next>
              <block type="variables_set" id="k~*@5pd2oz#e~q=nnzq6">
                <field name="VAR" id="J_sO@e2LThC4)euuGaIn">Win Amount</field>
                <value name="VALUE">
                  <block type="math_number" id="@Rt)nYJs-ARF8;nQmJ`e">
                    <field name="NUM">0.35</field>
                  </block>
                </value>
                <next>
                  <block type="variables_set" id="m+[ERt=8(CZ?zBOmv=sc">
                    <field name="VAR" id="Cr`aM/i9kt_5gWTJdeop">Initial Amount</field>
                    <value name="VALUE">
                      <block type="math_number" id="q~4Bc={-y7mzli0CH3I1">
                        <field name="NUM">0.35</field>
                      </block>
                    </value>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </next>
      </block>
    </statement>
    <statement name="SUBMARKET">
      <block type="trade_definition_tradeoptions" id="AJP4sSWk0U3WwVawD59?">
        <mutation xmlns="http://www.w3.org/1999/xhtml" has_first_barrier="false" has_second_barrier="false" has_prediction="false"></mutation>
        <field name="DURATIONTYPE_LIST">t</field>
        <value name="DURATION">
          <block type="math_number" id="r#L*.@8fI(FC.H3GmP)F">
            <field name="NUM">1</field>
          </block>
        </value>
        <value name="AMOUNT">
          <block type="variables_get" id="1T+jO=$wc@Oxg,-~uG3R">
            <field name="VAR" id="Cr`aM/i9kt_5gWTJdeop">Initial Amount</field>
          </block>
        </value>
      </block>
    </statement>
  </block>
  <block type="after_purchase" id="xTQg;1n?0,QIrZD9CQ:A" x="1447" y="0">
    <statement name="AFTERPURCHASE_STACK">
      <block type="variables_set" id="8agCpQY@UlQB#EeH`D[=">
        <field name="VAR" id="W85mq?KQPPq=M}Gbowq,">confirm_buy</field>
        <value name="VALUE">
          <block type="logic_boolean" id="~y..YN.d}nq8-n_DV@_,">
            <field name="BOOL">FALSE</field>
          </block>
        </value>
        <next>
          <block type="variables_set" id="cYx@#M:%w6E0e.:vMJyy">
            <field name="VAR" id="f5RncE:Nv!r(gN/kx3Ux">confirm_sell</field>
            <value name="VALUE">
              <block type="logic_boolean" id=")X}Q]=!~uI-V7Pq5pQDg">
                <field name="BOOL">FALSE</field>
              </block>
            </value>
            <next>
              <block type="variables_set" id="=u3vYwJ8Bh,]j*yY!,0G">
                <field name="VAR" id="rSWvU+{*:EmViRi~y6(W">final_buy</field>
                <value name="VALUE">
                  <block type="logic_boolean" id="+/^390ES:sT/uR$7Sv?w">
                    <field name="BOOL">FALSE</field>
                  </block>
                </value>
                <next>
                  <block type="variables_set" id="xoMqN@[)daE]}-nvk]e`">
                    <field name="VAR" id="?6{q@1dMn1rUO}Wdpo%a">final_sell</field>
                    <value name="VALUE">
                      <block type="logic_boolean" id="/~itl{hfh=FU2o}JEXm+">
                        <field name="BOOL">FALSE</field>
                      </block>
                    </value>
                    <next>
                      <block type="controls_if" id="gLMTdTfZe+DH~)[y@|6C">
                        <mutation xmlns="http://www.w3.org/1999/xhtml" else="1"></mutation>
                        <value name="IF0">
                          <block type="contract_check_result" id="6R-A((Bab4qQcs$ny~!l">
                            <field name="CHECK_RESULT">win</field>
                          </block>
                        </value>
                        <statement name="DO0">
                          <block type="text_join" id="8TiI(Q3:5qhx*~t!JVa%">
                            <field name="VARIABLE" id="I)3XQMar#(1p;_oOC!KS">text1</field>
                            <statement name="STACK">
                              <block type="text_statement" id="R;^hAPPU(QCcr4#SOlq8">
                                <value name="TEXT">
                                  <shadow type="text" id="I]2_dB/$77T|Z3R-Bdg7">
                                    <field name="TEXT"></field>
                                  </shadow>
                                  <block type="text" id="jk}oJ}h[:J)jB[DLs226">
                                    <field name="TEXT">Won:</field>
                                  </block>
                                </value>
                                <next>
                                  <block type="text_statement" id="@6l4YQfc2,|AB(]+z=g]">
                                    <value name="TEXT">
                                      <shadow type="text" id="@?C}!oDp[4OnSGKUnNDn">
                                        <field name="TEXT"></field>
                                      </shadow>
                                      <block type="read_details" id="mH`-=VwF1mg-V*xbfCdu">
                                        <field name="DETAIL_INDEX">4</field>
                                      </block>
                                    </value>
                                  </block>
                                </next>
                              </block>
                            </statement>
                            <next>
                              <block type="notify" id="SsuUtI$^tTer}}(kvIN-">
                                <field name="NOTIFICATION_TYPE">success</field>
                                <field name="NOTIFICATION_SOUND">silent</field>
                                <value name="MESSAGE">
                                  <block type="variables_get" id="!6b*Z2:Ge+pM1An]QZ%m">
                                    <field name="VAR" id="I)3XQMar#(1p;_oOC!KS">text1</field>
                                  </block>
                                </value>
                                <next>
                                  <block type="variables_set" id="WGiP/6gIf|gtc7XWvTE5">
                                    <field name="VAR" id="Cr`aM/i9kt_5gWTJdeop">Initial Amount</field>
                                    <value name="VALUE">
                                      <block type="variables_get" id="N#)bgI.iGi.k*1o7U#(.">
                                        <field name="VAR" id="J_sO@e2LThC4)euuGaIn">Win Amount</field>
                                      </block>
                                    </value>
                                  </block>
                                </next>
                              </block>
                            </next>
                          </block>
                        </statement>
                        <statement name="ELSE">
                          <block type="text_join" id="JV`tb|.E_0M,`;]#VpZi">
                            <field name="VARIABLE" id="hawGi,Q;JJ/3,_PGzul[">text2</field>
                            <statement name="STACK">
                              <block type="text_statement" id="h0xm1)`QH1-UuN!iS34P">
                                <value name="TEXT">
                                  <shadow type="text" id="h;%)PIyK4|9n97t8X.fJ">
                                    <field name="TEXT"></field>
                                  </shadow>
                                  <block type="text" id="__?F=haP({A5mdpT9|50">
                                    <field name="TEXT">Lost: </field>
                                  </block>
                                </value>
                                <next>
                                  <block type="text_statement" id="P$1.ZUOx!}LPh9jq[,E:">
                                    <value name="TEXT">
                                      <shadow type="text" id="?WB*n%C7ykjtjtHHH2Vf">
                                        <field name="TEXT"></field>
                                      </shadow>
                                      <block type="math_single" id="D?d/8RZ6^qgB|5nF9G1e">
                                        <field name="OP">ABS</field>
                                        <value name="NUM">
                                          <shadow type="math_number" id="y~G]ZLYH*t$#r~)($N+k">
                                            <field name="NUM">9</field>
                                          </shadow>
                                          <block type="read_details" id="BiFEqZ0nMW]X?vW7[+.3">
                                            <field name="DETAIL_INDEX">4</field>
                                          </block>
                                        </value>
                                      </block>
                                    </value>
                                  </block>
                                </next>
                              </block>
                            </statement>
                            <next>
                              <block type="notify" id="0;3LA9UpY}uOy3XE5UiK">
                                <field name="NOTIFICATION_TYPE">warn</field>
                                <field name="NOTIFICATION_SOUND">silent</field>
                                <value name="MESSAGE">
                                  <block type="variables_get" id="8)D,omG,EiU[3J_caz`1">
                                    <field name="VAR" id="hawGi,Q;JJ/3,_PGzul[">text2</field>
                                  </block>
                                </value>
                                <next>
                                  <block type="math_change" id=".s+]dZ2?Z}bPZYa[zIrl">
                                    <field name="VAR" id="Cr`aM/i9kt_5gWTJdeop">Initial Amount</field>
                                    <value name="DELTA">
                                      <shadow type="math_number" id="67B(3:h/5b}UUaBBAZ0E">
                                        <field name="NUM">1</field>
                                      </shadow>
                                      <block type="math_arithmetic" id="dz/VJaH,euMRwc:q?S2b">
                                        <field name="OP">MULTIPLY</field>
                                        <value name="A">
                                          <shadow type="math_number" id="B3-0r(%;9)Nduwj7RvzT">
                                            <field name="NUM">1</field>
                                          </shadow>
                                          <block type="math_single" id=":=$KQ63wGEO7b=+%c1w6">
                                            <field name="OP">ABS</field>
                                            <value name="NUM">
                                              <shadow type="math_number" id="ByNo`nOBuX@^3cUgH@zL">
                                                <field name="NUM">9</field>
                                              </shadow>
                                              <block type="read_details" id="I5+UclIyY|.9XXv7r)|x">
                                                <field name="DETAIL_INDEX">4</field>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                        <value name="B">
                                          <shadow type="math_number" id="%|=/j+SLe]E_/Jr_,gm4">
                                            <field name="NUM">1</field>
                                          </shadow>
                                          <block type="math_number" id="QcGdUw_r@T|/Hhfae+p/">
                                            <field name="NUM">1.098</field>
                                          </block>
                                        </value>
                                      </block>
                                    </value>
                                    <next>
                                      <block type="controls_if" id="Vm]^^q3/vW{OW7jt#1i%">
                                        <value name="IF0">
                                          <block type="logic_compare" id="6XZGoxONZWsJBPCIu.r5">
                                            <field name="OP">GTE</field>
                                            <value name="A">
                                              <block type="math_single" id="zYg?K`YHS2Ff!4irn,$q">
                                                <field name="OP">ABS</field>
                                                <value name="NUM">
                                                  <shadow type="math_number" id="R_Jz{~S]+4LWoYAs/Re5">
                                                    <field name="NUM">9</field>
                                                  </shadow>
                                                  <block type="read_details" id=",euoa9N|eG+oq9LIM/a;">
                                                    <field name="DETAIL_INDEX">4</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </value>
                                            <value name="B">
                                              <block type="variables_get" id="p4*G:u3*?c2wl;SPvfqN">
                                                <field name="VAR" id="P${QsG.49i3t/T2Y{ORI">Max Loss Amount</field>
                                              </block>
                                            </value>
                                          </block>
                                        </value>
                                        <statement name="DO0">
                                          <block type="variables_set" id="TaFwfk)Od{CC^7-.Fu93">
                                            <field name="VAR" id="Cr`aM/i9kt_5gWTJdeop">Initial Amount</field>
                                            <value name="VALUE">
                                              <block type="variables_get" id="8%Ou:U6m}PEn9S/)jo+r">
                                                <field name="VAR" id="J_sO@e2LThC4)euuGaIn">Win Amount</field>
                                              </block>
                                            </value>
                                          </block>
                                        </statement>
                                      </block>
                                    </next>
                                  </block>
                                </next>
                              </block>
                            </next>
                          </block>
                        </statement>
                        <next>
                          <block type="text_join" id=".J8D#i0ny(7@;zowV#D,">
                            <field name="VARIABLE" id="loET/e:aUs+;odJPKJSq">text3</field>
                            <statement name="STACK">
                              <block type="text_statement" id="rziLd/6yP~en?iddkh,l">
                                <value name="TEXT">
                                  <shadow type="text" id="qrjclD{MqK~L@%h-_bH!">
                                    <field name="TEXT"></field>
                                  </shadow>
                                  <block type="text" id="@;Kw]h`XB,79HdHgO0(a">
                                    <field name="TEXT">Total Profit: </field>
                                  </block>
                                </value>
                                <next>
                                  <block type="text_statement" id="(#IKssVfB0]:=YWwk0u+">
                                    <value name="TEXT">
                                      <shadow type="text" id="!Z4lkJ5dUTwga5+~#_E8">
                                        <field name="TEXT"></field>
                                      </shadow>
                                      <block type="total_profit" id="5o]5^r(VOy%17o}=)vE`"></block>
                                    </value>
                                  </block>
                                </next>
                              </block>
                            </statement>
                            <next>
                              <block type="notify" id="-0dzqt*2+}GQrlB9kxHI">
                                <field name="NOTIFICATION_TYPE">info</field>
                                <field name="NOTIFICATION_SOUND">silent</field>
                                <value name="MESSAGE">
                                  <block type="variables_get" id="Hx;Po!v`:^rt(AnGp,K6">
                                    <field name="VAR" id="loET/e:aUs+;odJPKJSq">text3</field>
                                  </block>
                                </value>
                                <next>
                                  <block type="controls_if" id="@L9VH?S7ZENJ+W|^td=r">
                                    <mutation xmlns="http://www.w3.org/1999/xhtml" else="1"></mutation>
                                    <value name="IF0">
                                      <block type="logic_compare" id="`NPK$Hxt`Es*Aq8*hf0)">
                                        <field name="OP">LT</field>
                                        <value name="A">
                                          <block type="total_profit" id="PqL85,qG44H^NKD)tLS;"></block>
                                        </value>
                                        <value name="B">
                                          <block type="variables_get" id="^5`N~G)4i~-OYo@]]#Ik">
                                            <field name="VAR" id="_^K%$ZT3iAJ0r,=Y)t{e">Expected Profit</field>
                                          </block>
                                        </value>
                                      </block>
                                    </value>
                                    <statement name="DO0">
                                      <block type="trade_again" id="R}t`:sA(_r57Tl3z;qRJ"></block>
                                    </statement>
                                    <statement name="ELSE">
                                      <block type="text_join" id="DQao}(~F:Bm#la0q!I6o">
                                        <field name="VARIABLE" id="5t%R8/wO^;qaB|m{{J9[">text4</field>
                                        <statement name="STACK">
                                          <block type="text_statement" id="+QkZe.;n1{1B_a:MD98X">
                                            <value name="TEXT">
                                              <shadow type="text" id="u|RdNC1/34N36Ve4@R8=">
                                                <field name="TEXT"></field>
                                              </shadow>
                                              <block type="text" id="{7o}AN052n6E0w7x|AC2">
                                                <field name="TEXT">Done! Total profit: </field>
                                              </block>
                                            </value>
                                            <next>
                                              <block type="text_statement" id="@F:~5F_{]gq.?(]bTNO1">
                                                <value name="TEXT">
                                                  <shadow type="text" id="v*3]fXlQ![WG()1}H[f$">
                                                    <field name="TEXT"></field>
                                                  </shadow>
                                                  <block type="total_profit" id="[B/AlCu77g-[ZgB,SQMK"></block>
                                                </value>
                                              </block>
                                            </next>
                                          </block>
                                        </statement>
                                        <next>
                                          <block type="text_print" id="td6z*FI8z2hqj+SmBDTv">
                                            <value name="TEXT">
                                              <shadow type="text" id="43l;snhvr*mq(]_:%DU+">
                                                <field name="TEXT">abc</field>
                                              </shadow>
                                              <block type="variables_get" id="uVjD:Argh5HQ-HOg+N5c">
                                                <field name="VAR" id="5t%R8/wO^;qaB|m{{J9[">text4</field>
                                              </block>
                                            </value>
                                          </block>
                                        </next>
                                      </block>
                                    </statement>
                                  </block>
                                </next>
                              </block>
                            </next>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </next>
      </block>
    </statement>
  </block>
  <block type="before_purchase" id="{IIr#Od}Wjg9Dh~_X+P." deletable="false" x="0" y="772">
    <statement name="BEFOREPURCHASE_STACK">
      <block type="bb_statement" id="tv+Ck#6(.uL([{J:ba4}">
        <field name="VARIABLE" id="lb:;T7(!b|F%_^%##%yn">ema_high</field>
        <field name="BBRESULT_LIST">1</field>
        <statement name="STATEMENT">
          <block type="input_list" id="Kbx3H5fSx@Vuh)q%rv0%" deletable="false" movable="false">
            <value name="INPUT_LIST">
              <block type="ticks" id="DV!]g?esYE`{xjZC[i(}"></block>
            </value>
            <next>
              <block type="period" id="*6:k=_J9y@wQF`th`}};" deletable="false" movable="false">
                <value name="PERIOD">
                  <shadow type="math_number" id="j)P(w*vzt(YjEB06%brj">
                    <field name="NUM">15</field>
                  </shadow>
                </value>
                <next>
                  <block type="std_dev_multiplier_up" id=")d?jLag(N4BR)lRPM1gT" deletable="false" movable="false">
                    <value name="UPMULTIPLIER">
                      <shadow type="math_number" id="ewER8d?in]0l0;Bon`sl">
                        <field name="NUM">2</field>
                      </shadow>
                    </value>
                    <next>
                      <block type="std_dev_multiplier_down" id="xk(7Pe4oVlKpVf-#=F.S" deletable="false" movable="false">
                        <value name="DOWNMULTIPLIER">
                          <shadow type="math_number" id="BwruwImgd7jh2fI9RUpW">
                            <field name="NUM">2</field>
                          </shadow>
                        </value>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </statement>
        <next>
          <block type="bb_statement" id="EC.@LWf1gQyNb-RfS-7F">
            <field name="VARIABLE" id="x4#5JPs2*L*8h3AbMKjp">bb_mid</field>
            <field name="BBRESULT_LIST">0</field>
            <statement name="STATEMENT">
              <block type="input_list" id="[s,|@S1_p:Tm6t5Z?[pL" deletable="false" movable="false">
                <value name="INPUT_LIST">
                  <block type="ticks" id="*;$)HnQNb?,!(!pO%GG`"></block>
                </value>
                <next>
                  <block type="period" id="v1O4=mpn0,2=)Uzq+a=7" deletable="false" movable="false">
                    <value name="PERIOD">
                      <shadow type="math_number" id="U6);=:_cJ;1}5)9.N^Lc">
                        <field name="NUM">10</field>
                      </shadow>
                    </value>
                    <next>
                      <block type="std_dev_multiplier_up" id="$eS(Q:q-e|@KJ:k?q@FR" deletable="false" movable="false">
                        <value name="UPMULTIPLIER">
                          <shadow type="math_number" id="[:$|i#~%VZwt^zL?MQ[%">
                            <field name="NUM">2</field>
                          </shadow>
                        </value>
                        <next>
                          <block type="std_dev_multiplier_down" id=")0|-IgVJa852nEDvFN~w" deletable="false" movable="false">
                            <value name="DOWNMULTIPLIER">
                              <shadow type="math_number" id="M*]F((,u=M`Mhnl7e%1`">
                                <field name="NUM">2</field>
                              </shadow>
                            </value>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </statement>
            <next>
              <block type="bb_statement" id="kouR~:zzqQ`up(n314~G">
                <field name="VARIABLE" id=".IG]LH|qsDGx+7{U-_cu">bb_low</field>
                <field name="BBRESULT_LIST">2</field>
                <statement name="STATEMENT">
                  <block type="input_list" id="oumFA*T0K0]:jl,4i61V" deletable="false" movable="false">
                    <value name="INPUT_LIST">
                      <block type="ticks" id="PteR+50?/ztd}~yXXb2^"></block>
                    </value>
                    <next>
                      <block type="period" id="pm6:1dKS~.hSgk8r$H%m" deletable="false" movable="false">
                        <value name="PERIOD">
                          <shadow type="math_number" id="ZAjsRQ^!Ogcqe@j//cNH">
                            <field name="NUM">5</field>
                          </shadow>
                        </value>
                        <next>
                          <block type="std_dev_multiplier_up" id="JG-[pcFihFM$c~Ek9Y@8" deletable="false" movable="false">
                            <value name="UPMULTIPLIER">
                              <shadow type="math_number" id=",^mo@vepD|nEiF5*oLv-">
                                <field name="NUM">2</field>
                              </shadow>
                            </value>
                            <next>
                              <block type="std_dev_multiplier_down" id="%Jy?Ln8;,9q(r!Nke:b$" deletable="false" movable="false">
                                <value name="DOWNMULTIPLIER">
                                  <shadow type="math_number" id="Wj?tL8?*Att_/JW9fG|F">
                                    <field name="NUM">2</field>
                                  </shadow>
                                </value>
                              </block>
                            </next>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </statement>
                <next>
                  <block type="ema_statement" id=")#P3U9WRnTY9yyUXRDa{">
                    <field name="VARIABLE" id="lb:;T7(!b|F%_^%##%yn">ema_high</field>
                    <statement name="STATEMENT">
                      <block type="input_list" id="t#I0vOCAq-lA0ZLWU`wn" deletable="false" movable="false">
                        <value name="INPUT_LIST">
                          <block type="ticks" id="IDi#s$Q:UlN/+_391KB~"></block>
                        </value>
                        <next>
                          <block type="period" id="+nLs7rZWwyeN#pBItFI]" deletable="false" movable="false">
                            <value name="PERIOD">
                              <shadow type="math_number" id="9uEG?O2V@7Am[Ww?or?5">
                                <field name="NUM">15</field>
                              </shadow>
                            </value>
                          </block>
                        </next>
                      </block>
                    </statement>
                    <next>
                      <block type="ema_statement" id=".htVKwe4=/uHH1,=5ruz">
                        <field name="VARIABLE" id="ficbIddKcG0H,-jqM$7X">ema_mid</field>
                        <statement name="STATEMENT">
                          <block type="input_list" id="[JsQ+p4(A|Us$a20(zA#" deletable="false" movable="false">
                            <value name="INPUT_LIST">
                              <block type="ticks" id="QC0{94-qU8oDS_{S~uWl"></block>
                            </value>
                            <next>
                              <block type="period" id="UGeiyrBM2uj*?0c^Qlnq" deletable="false" movable="false">
                                <value name="PERIOD">
                                  <shadow type="math_number" id="XhHgh]0f?QxMN!X[||9M">
                                    <field name="NUM">10</field>
                                  </shadow>
                                </value>
                              </block>
                            </next>
                          </block>
                        </statement>
                        <next>
                          <block type="ema_statement" id="/z!%y)G23UO#wU~1B7`O">
                            <field name="VARIABLE" id="t@%I.Ll]DNl^^rVCfI#R">ema_low</field>
                            <statement name="STATEMENT">
                              <block type="input_list" id="0oLU[$4A!B!..!B}u9OB" deletable="false" movable="false">
                                <value name="INPUT_LIST">
                                  <block type="ticks" id="tJH*s9U9Y[707[o$_MpT"></block>
                                </value>
                                <next>
                                  <block type="period" id="ER^|d$}0z0@IoL;{6R$S" deletable="false" movable="false">
                                    <value name="PERIOD">
                                      <shadow type="math_number" id="f0a,xm/^!*`pQx/T73FD">
                                        <field name="NUM">5</field>
                                      </shadow>
                                    </value>
                                  </block>
                                </next>
                              </block>
                            </statement>
                            <next>
                              <block type="rsi_statement" id="b?9C%JxAe*70^-kiOh%)">
                                <field name="VARIABLE" id="P);w$.oDv0edq+xZr8^q">RSI</field>
                                <statement name="STATEMENT">
                                  <block type="input_list" id="4tdqW,|Vuk}p2!4lLOL=" deletable="false" movable="false">
                                    <value name="INPUT_LIST">
                                      <block type="ticks" id="u(F(~+^qS_h*#GaRP)jH"></block>
                                    </value>
                                    <next>
                                      <block type="period" id="cP|QELfdduDom+22:7d7" deletable="false" movable="false">
                                        <value name="PERIOD">
                                          <block type="math_number" id="^,rU`y)KvM84icWIux*D">
                                            <field name="NUM">9</field>
                                          </block>
                                        </value>
                                      </block>
                                    </next>
                                  </block>
                                </statement>
                                <next>
                                  <block type="variables_set" id="*U5HN~O_tEI,UBa0/~_S">
                                    <field name="VAR" id="P);w$.oDv0edq+xZr8^q">RSI</field>
                                    <value name="VALUE">
                                      <block type="variables_get" id="l,T=]dF:HJ#:etA%(?x{">
                                        <field name="VAR" id="P);w$.oDv0edq+xZr8^q">RSI</field>
                                      </block>
                                    </value>
                                    <next>
                                      <block type="text_join" id="{Y0`kQPkwU?;44d={2Nz">
                                        <field name="VARIABLE" id="(S/imNt40Dig^U{0v.[:">text</field>
                                        <statement name="STACK">
                                          <block type="text_statement" id="ovz,ZiS(N|d}KH=GxJ[$">
                                            <value name="TEXT">
                                              <shadow type="text" id=":u@vVxuP]N*p|phLIBvY">
                                                <field name="TEXT"></field>
                                              </shadow>
                                              <block type="text" id="Yt9j)CF8HO#+HNhnOrih">
                                                <field name="TEXT">RSI: </field>
                                              </block>
                                            </value>
                                            <next>
                                              <block type="text_statement" id="cU)*e-ZP`Dg=mp!9AyVU">
                                                <value name="TEXT">
                                                  <shadow type="text" id="czf^_-9(;dd`fYf{y6Hp">
                                                    <field name="TEXT"></field>
                                                  </shadow>
                                                  <block type="variables_get" id="Y8h2+$vRUQ4G+?gHfhY~">
                                                    <field name="VAR" id="P);w$.oDv0edq+xZr8^q">RSI</field>
                                                  </block>
                                                </value>
                                              </block>
                                            </next>
                                          </block>
                                        </statement>
                                        <next>
                                          <block type="notify" id="Q#35Qw20Y7alwPcJO7zn">
                                            <field name="NOTIFICATION_TYPE">success</field>
                                            <field name="NOTIFICATION_SOUND">silent</field>
                                            <value name="MESSAGE">
                                              <block type="variables_get" id="baFf{z|:)3ziL-5MTj$!">
                                                <field name="VAR" id="(S/imNt40Dig^U{0v.[:">text</field>
                                              </block>
                                            </value>
                                            <next>
                                              <block type="controls_if" id="fm[i5!m%_pUX,SX,DN45">
                                                <value name="IF0">
                                                  <block type="logic_operation" id="3XJ9O;,+WSEvIEiX`xZ{">
                                                    <field name="OP">AND</field>
                                                    <value name="A">
                                                      <block type="logic_compare" id="6{TNcfsR~w(x7*q(ya;T">
                                                        <field name="OP">LT</field>
                                                        <value name="A">
                                                          <block type="variables_get" id="iU6*}$kO_QPj2H[xn{SW">
                                                            <field name="VAR" id="P);w$.oDv0edq+xZr8^q">RSI</field>
                                                          </block>
                                                        </value>
                                                        <value name="B">
                                                          <block type="math_number" id="-d^R(rESkqxpd/5uzG(+">
                                                            <field name="NUM">50</field>
                                                          </block>
                                                        </value>
                                                      </block>
                                                    </value>
                                                    <value name="B">
                                                      <block type="logic_operation" id="l8%/1L(7)jM^z41`*rY4">
                                                        <field name="OP">AND</field>
                                                        <value name="A">
                                                          <block type="logic_compare" id="241F#eEG^+)kjZX*G@|c">
                                                            <field name="OP">LT</field>
                                                            <value name="A">
                                                              <block type="lists_getIndex" id="Ly[wFYF;Fs@tf2C}mRuA">
                                                                <mutation xmlns="http://www.w3.org/1999/xhtml" statement="false" at="false"></mutation>
                                                                <field name="MODE">GET</field>
                                                                <field name="WHERE">LAST</field>
                                                                <value name="VALUE">
                                                                  <block type="ticks" id="foJH@4#Pi1MiiQo+[Olx"></block>
                                                                </value>
                                                              </block>
                                                            </value>
                                                            <value name="B">
                                                              <block type="variables_get" id="Hs5:x]S{MNy50!SvW+sr">
                                                                <field name="VAR" id="x4#5JPs2*L*8h3AbMKjp">bb_mid</field>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </value>
                                                        <value name="B">
                                                          <block type="logic_compare" id="MARz61y),4PBp5qqaBu#">
                                                            <field name="OP">LTE</field>
                                                            <value name="A">
                                                              <block type="variables_get" id="[(wIrwb+!)B[zGVJBnke">
                                                                <field name="VAR" id=".IG]LH|qsDGx+7{U-_cu">bb_low</field>
                                                              </block>
                                                            </value>
                                                            <value name="B">
                                                              <block type="variables_get" id="fD^oAbS5%q(ZH)r[WhGc">
                                                                <field name="VAR" id="x4#5JPs2*L*8h3AbMKjp">bb_mid</field>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </value>
                                                      </block>
                                                    </value>
                                                  </block>
                                                </value>
                                                <statement name="DO0">
                                                  <block type="variables_set" id=":+lH{Qx0p2cQFJkMZW??">
                                                    <field name="VAR" id="W85mq?KQPPq=M}Gbowq,">confirm_buy</field>
                                                    <value name="VALUE">
                                                      <block type="logic_boolean" id="+5p9l0Y_dT`|oB$1L!.S">
                                                        <field name="BOOL">TRUE</field>
                                                      </block>
                                                    </value>
                                                    <next>
                                                      <block type="text_join" id="}z()?.-QNsk+9yb?V@w3">
                                                        <field name="VARIABLE" id="yrsK]*nMA`[.ILEFWbFa">text_1</field>
                                                        <statement name="STACK">
                                                          <block type="text_statement" id="m`sq#x4wj%H]#m+9guPZ">
                                                            <value name="TEXT">
                                                              <shadow type="text" id="~^pOxaJ@MWNN}+S%,hTF">
                                                                <field name="TEXT">confirm buy</field>
                                                              </shadow>
                                                            </value>
                                                            <next>
                                                              <block type="text_statement" id="8H=kL`]LFGkqN=60sI:a">
                                                                <value name="TEXT">
                                                                  <shadow type="text" id="!;6?11Tb)$@}Wc/95KLR">
                                                                    <field name="TEXT">confirm buy</field>
                                                                  </shadow>
                                                                  <block type="variables_get" id="!AErWyK{P]Q)qp~,s{sn">
                                                                    <field name="VAR" id="W85mq?KQPPq=M}Gbowq,">confirm_buy</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </next>
                                                          </block>
                                                        </statement>
                                                        <next>
                                                          <block type="notify" id="h-r[O.sKw|=cL/8[[ReO">
                                                            <field name="NOTIFICATION_TYPE">info</field>
                                                            <field name="NOTIFICATION_SOUND">silent</field>
                                                            <value name="MESSAGE">
                                                              <shadow type="text" id="ey~!nd%]p-A0?fj|];gS">
                                                                <field name="TEXT">abc</field>
                                                              </shadow>
                                                              <block type="variables_get" id="];,enu!O4`ef1A4hi2Ky">
                                                                <field name="VAR" id="yrsK]*nMA`[.ILEFWbFa">text_1</field>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </next>
                                                      </block>
                                                    </next>
                                                  </block>
                                                </statement>
                                                <next>
                                                  <block type="controls_if" id="%F2^H~B7w?nH5n$9qN$b">
                                                    <value name="IF0">
                                                      <block type="logic_operation" id="68/s$0qnmMyF($UBylFR">
                                                        <field name="OP">AND</field>
                                                        <value name="A">
                                                          <block type="logic_compare" id="DQr^~GbPv{r?PTPe1+5^">
                                                            <field name="OP">GT</field>
                                                            <value name="A">
                                                              <block type="variables_get" id="bjp`$)~g0FFix2-E_l0X">
                                                                <field name="VAR" id="P);w$.oDv0edq+xZr8^q">RSI</field>
                                                              </block>
                                                            </value>
                                                            <value name="B">
                                                              <block type="math_number" id="I#duD%Q)=+Cjw|T2-Z9F">
                                                                <field name="NUM">50</field>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </value>
                                                        <value name="B">
                                                          <block type="logic_operation" id="VY-^Z|Ix}R`{5,g{eR37">
                                                            <field name="OP">AND</field>
                                                            <value name="A">
                                                              <block type="logic_compare" id="J2-86p}Ksqf$TO5-{gI`">
                                                                <field name="OP">LTE</field>
                                                                <value name="A">
                                                                  <block type="lists_getIndex" id="gFvG]y.rVZZ$4dK^$eS.">
                                                                    <mutation xmlns="http://www.w3.org/1999/xhtml" statement="false" at="false"></mutation>
                                                                    <field name="MODE">GET</field>
                                                                    <field name="WHERE">LAST</field>
                                                                    <value name="VALUE">
                                                                      <block type="ticks" id="u]]rWKKj4ioUF/L5$1P{"></block>
                                                                    </value>
                                                                  </block>
                                                                </value>
                                                                <value name="B">
                                                                  <block type="variables_get" id="`XFxP:|e_6BUz{Wi%M6{">
                                                                    <field name="VAR" id="x4#5JPs2*L*8h3AbMKjp">bb_mid</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </value>
                                                            <value name="B">
                                                              <block type="logic_compare" id="[)ve3B.I1oQB2?(Q~Cs~">
                                                                <field name="OP">LTE</field>
                                                                <value name="A">
                                                                  <block type="variables_get" id="z,ZCprJEuf}^F}aNBw|G">
                                                                    <field name="VAR" id="5bJ`h_VFI5+1BF3[iLa*">bb_high</field>
                                                                  </block>
                                                                </value>
                                                                <value name="B">
                                                                  <block type="variables_get" id="H2A8L#e~|R*q@65`eyo%">
                                                                    <field name="VAR" id="x4#5JPs2*L*8h3AbMKjp">bb_mid</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </value>
                                                      </block>
                                                    </value>
                                                    <statement name="DO0">
                                                      <block type="text_join" id=")4GVq@uG,jJPm+X+mYeg">
                                                        <field name="VARIABLE" id="1sJ}oeqKGJuzhc,+sSsL">text_2</field>
                                                        <statement name="STACK">
                                                          <block type="text_statement" id="[z0M6!8=@]`Kx4=Tem61">
                                                            <value name="TEXT">
                                                              <shadow type="text" id="[rn+z^?9~l2MdBm?jA,t">
                                                                <field name="TEXT">confirm sell</field>
                                                              </shadow>
                                                            </value>
                                                            <next>
                                                              <block type="text_statement" id="QI{2x8UM`iNLsSPcO!q[">
                                                                <value name="TEXT">
                                                                  <shadow type="text" id="5Vz~JZii+Pv[kD~s.xc0">
                                                                    <field name="TEXT"></field>
                                                                  </shadow>
                                                                  <block type="variables_get" id="*-0lJXQVe-6)o_n^xyxa">
                                                                    <field name="VAR" id="f5RncE:Nv!r(gN/kx3Ux">confirm_sell</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </next>
                                                          </block>
                                                        </statement>
                                                        <next>
                                                          <block type="notify" id="B[UY8A]v8JAtN:#$~TFy">
                                                            <field name="NOTIFICATION_TYPE">error</field>
                                                            <field name="NOTIFICATION_SOUND">silent</field>
                                                            <value name="MESSAGE">
                                                              <shadow type="text" id="LeP52$Xthf@T_]C}jDV$">
                                                                <field name="TEXT">abc</field>
                                                              </shadow>
                                                              <block type="variables_get" id=";%P|dVqHc8{r_.8LQ3$|">
                                                                <field name="VAR" id="1sJ}oeqKGJuzhc,+sSsL">text_2</field>
                                                              </block>
                                                            </value>
                                                            <next>
                                                              <block type="variables_set" id="ycm/5t?@~-%6=/0Oo]/w">
                                                                <field name="VAR" id="f5RncE:Nv!r(gN/kx3Ux">confirm_sell</field>
                                                                <value name="VALUE">
                                                                  <block type="logic_boolean" id="Ug/0)ZxNA}HExzFnKR5G">
                                                                    <field name="BOOL">TRUE</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </next>
                                                          </block>
                                                        </next>
                                                      </block>
                                                    </statement>
                                                    <next>
                                                      <block type="controls_if" id="k,~Oiee0ic6x19kGg3^@">
                                                        <value name="IF0">
                                                          <block type="logic_compare" id="TK6AJFhnm)$RdX#Iw/(k">
                                                            <field name="OP">EQ</field>
                                                            <value name="A">
                                                              <block type="variables_get" id="K,s]+!8NbyL]f]Yc$7?6">
                                                                <field name="VAR" id="W85mq?KQPPq=M}Gbowq,">confirm_buy</field>
                                                              </block>
                                                            </value>
                                                            <value name="B">
                                                              <block type="logic_boolean" id="(|cc#JIMMHu7tca6Xil7">
                                                                <field name="BOOL">TRUE</field>
                                                              </block>
                                                            </value>
                                                          </block>
                                                        </value>
                                                        <statement name="DO0">
                                                          <block type="controls_if" id="~BF3EEe3S.HHb_(FuK5F">
                                                            <value name="IF0">
                                                              <block type="logic_operation" id="B(+U~)$eODMR.Ytfi?D:">
                                                                <field name="OP">AND</field>
                                                                <value name="A">
                                                                  <block type="logic_compare" id="kIw~Y=lU*VEKh?v}[*OH">
                                                                    <field name="OP">GT</field>
                                                                    <value name="A">
                                                                      <block type="lists_getIndex" id="{0aZY3*Y{$f9+o*)/rN.">
                                                                        <mutation xmlns="http://www.w3.org/1999/xhtml" statement="false" at="false"></mutation>
                                                                        <field name="MODE">GET</field>
                                                                        <field name="WHERE">LAST</field>
                                                                        <value name="VALUE">
                                                                          <block type="ticks" id=")kbV]wQW?N1$[3OOB}=|"></block>
                                                                        </value>
                                                                      </block>
                                                                    </value>
                                                                    <value name="B">
                                                                      <block type="variables_get" id="1f@4L*)BF]B6$WxWO~+0">
                                                                        <field name="VAR" id="lb:;T7(!b|F%_^%##%yn">ema_high</field>
                                                                      </block>
                                                                    </value>
                                                                  </block>
                                                                </value>
                                                                <value name="B">
                                                                  <block type="logic_compare" id="UPf_|Hs_(dx%d$K5StrK">
                                                                    <field name="OP">GTE</field>
                                                                    <value name="A">
                                                                      <block type="variables_get" id="]RHd!z^w~(2N@lwE5AUU">
                                                                        <field name="VAR" id="lb:;T7(!b|F%_^%##%yn">ema_high</field>
                                                                      </block>
                                                                    </value>
                                                                    <value name="B">
                                                                      <block type="variables_get" id="H(X_vP/n{lqQ9lhUB5r#">
                                                                        <field name="VAR" id="ficbIddKcG0H,-jqM$7X">ema_mid</field>
                                                                      </block>
                                                                    </value>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </value>
                                                            <statement name="DO0">
                                                              <block type="variables_set" id="`NORQ.G;RVZ(1n4)vD3}">
                                                                <field name="VAR" id="rSWvU+{*:EmViRi~y6(W">final_buy</field>
                                                                <value name="VALUE">
                                                                  <block type="logic_boolean" id="I},dp8kWP,?MX+`xw:,Y">
                                                                    <field name="BOOL">TRUE</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </statement>
                                                          </block>
                                                        </statement>
                                                        <next>
                                                          <block type="controls_if" id="a!-GCF,k%Ij;6?7ZHQFD">
                                                            <value name="IF0">
                                                              <block type="logic_compare" id="{UjiCEU:(iTvX4y_v[BE">
                                                                <field name="OP">EQ</field>
                                                                <value name="A">
                                                                  <block type="variables_get" id="~GHI*:7r@pv][nv,=-CF">
                                                                    <field name="VAR" id="f5RncE:Nv!r(gN/kx3Ux">confirm_sell</field>
                                                                  </block>
                                                                </value>
                                                                <value name="B">
                                                                  <block type="logic_boolean" id="1)bW#Oa6!Jca*l-#d`R7">
                                                                    <field name="BOOL">TRUE</field>
                                                                  </block>
                                                                </value>
                                                              </block>
                                                            </value>
                                                            <statement name="DO0">
                                                              <block type="controls_if" id="kh{+)@C.R~LEZGU7,z*5">
                                                                <value name="IF0">
                                                                  <block type="logic_operation" id="7R9$u/rbiZD!1sbzWaYv">
                                                                    <field name="OP">AND</field>
                                                                    <value name="A">
                                                                      <block type="logic_compare" id="EF==wyG-F~A|z(ag)nJM">
                                                                        <field name="OP">LT</field>
                                                                        <value name="A">
                                                                          <block type="lists_getIndex" id="e?z=@e2k6PVR^H%]PU#3">
                                                                            <mutation xmlns="http://www.w3.org/1999/xhtml" statement="false" at="false"></mutation>
                                                                            <field name="MODE">GET</field>
                                                                            <field name="WHERE">LAST</field>
                                                                            <value name="VALUE">
                                                                              <block type="ticks" id="VkTd|pu|a_}t7Rq!!uEr"></block>
                                                                            </value>
                                                                          </block>
                                                                        </value>
                                                                        <value name="B">
                                                                          <block type="variables_get" id="pMq`h1-0C9c=1;d*N?+!">
                                                                            <field name="VAR" id="ficbIddKcG0H,-jqM$7X">ema_mid</field>
                                                                          </block>
                                                                        </value>
                                                                      </block>
                                                                    </value>
                                                                    <value name="B">
                                                                      <block type="logic_compare" id="Z5r5dCXobY.nz5arrk+]">
                                                                        <field name="OP">LTE</field>
                                                                        <value name="A">
                                                                          <block type="variables_get" id="r4VC(;XgemwBRW=9{{zM">
                                                                            <field name="VAR" id="t@%I.Ll]DNl^^rVCfI#R">ema_low</field>
                                                                          </block>
                                                                        </value>
                                                                        <value name="B">
                                                                          <block type="variables_get" id="[x-kG7*?/O+,c6ka09Q/">
                                                                            <field name="VAR" id="ficbIddKcG0H,-jqM$7X">ema_mid</field>
                                                                          </block>
                                                                        </value>
                                                                      </block>
                                                                    </value>
                                                                  </block>
                                                                </value>
                                                                <statement name="DO0">
                                                                  <block type="variables_set" id="fN_,d${oBNX/H2!g)$xu">
                                                                    <field name="VAR" id="?6{q@1dMn1rUO}Wdpo%a">final_sell</field>
                                                                    <value name="VALUE">
                                                                      <block type="logic_boolean" id="0/9{pO`B[+stDs:4o^X8">
                                                                        <field name="BOOL">TRUE</field>
                                                                      </block>
                                                                    </value>
                                                                  </block>
                                                                </statement>
                                                              </block>
                                                            </statement>
                                                            <next>
                                                              <block type="controls_if" id="uO8Y@nk#27POihe@s)au">
                                                                <value name="IF0">
                                                                  <block type="logic_compare" id="2dA5FYr!l1dS]R^PIlf#">
                                                                    <field name="OP">EQ</field>
                                                                    <value name="A">
                                                                      <block type="variables_get" id="Ki,oQso=*Vf^tMpn{%1g">
                                                                        <field name="VAR" id="rSWvU+{*:EmViRi~y6(W">final_buy</field>
                                                                      </block>
                                                                    </value>
                                                                    <value name="B">
                                                                      <block type="logic_boolean" id="E764.Q/)U7nEo%miqDo#">
                                                                        <field name="BOOL">TRUE</field>
                                                                      </block>
                                                                    </value>
                                                                  </block>
                                                                </value>
                                                                <statement name="DO0">
                                                                  <block type="text_join" id="5bVSt{T*1EnS6`j1/?VS">
                                                                    <field name="VARIABLE" id="{O*2nA--BG.dq#ykJF:[">text_4</field>
                                                                    <statement name="STACK">
                                                                      <block type="text_statement" id="+8[OXgg?X@tK{k.D6/:9">
                                                                        <value name="TEXT">
                                                                          <shadow type="text" id="fN/@*dP+_Vz~9HgEqxIZ">
                                                                            <field name="TEXT">final buy</field>
                                                                          </shadow>
                                                                        </value>
                                                                        <next>
                                                                          <block type="text_statement" id="EAurY]F@B/fN@:/r:VJB">
                                                                            <value name="TEXT">
                                                                              <shadow type="text" id="x(opI5eiWIHzY}n*4p(h">
                                                                                <field name="TEXT">abc</field>
                                                                              </shadow>
                                                                              <block type="variables_get" id="J[(.456g2p4a-m_9bMUT">
                                                                                <field name="VAR" id="rSWvU+{*:EmViRi~y6(W">final_buy</field>
                                                                              </block>
                                                                            </value>
                                                                          </block>
                                                                        </next>
                                                                      </block>
                                                                    </statement>
                                                                    <next>
                                                                      <block type="notify" id="2LS$IssyW~O}2vz|MO|p">
                                                                        <field name="NOTIFICATION_TYPE">warn</field>
                                                                        <field name="NOTIFICATION_SOUND">silent</field>
                                                                        <value name="MESSAGE">
                                                                          <shadow type="text" id=":GFV2[QV;6sCW4RN49Iz">
                                                                            <field name="TEXT">abc</field>
                                                                          </shadow>
                                                                          <block type="variables_get" id="O=4od0w!I]AFu_she2]Y">
                                                                            <field name="VAR" id="{O*2nA--BG.dq#ykJF:[">text_4</field>
                                                                          </block>
                                                                        </value>
                                                                        <next>
                                                                          <block type="purchase" id="y@sj$jL$Fwc)hU0O[SZ`">
                                                                            <field name="PURCHASE_LIST">CALL</field>
                                                                          </block>
                                                                        </next>
                                                                      </block>
                                                                    </next>
                                                                  </block>
                                                                </statement>
                                                                <next>
                                                                  <block type="controls_if" id="5kiKyL-guTG*9LzUdP/p">
                                                                    <value name="IF0">
                                                                      <block type="logic_compare" id="c+-YMdsayl#vOix]$abq">
                                                                        <field name="OP">EQ</field>
                                                                        <value name="A">
                                                                          <block type="variables_get" id="U5}/JlP}ay4]]K~BI28i">
                                                                            <field name="VAR" id="?6{q@1dMn1rUO}Wdpo%a">final_sell</field>
                                                                          </block>
                                                                        </value>
                                                                        <value name="B">
                                                                          <block type="logic_boolean" id="mZcwkjiWP?:!0*J$q+UQ">
                                                                            <field name="BOOL">TRUE</field>
                                                                          </block>
                                                                        </value>
                                                                      </block>
                                                                    </value>
                                                                    <statement name="DO0">
                                                                      <block type="text_join" id="eeI$O%d=U5gkaUWn+4Br">
                                                                        <field name="VARIABLE" id="U_|ZtI3=Zjv=JdeDgwf2">text_3</field>
                                                                        <statement name="STACK">
                                                                          <block type="text_statement" id="M#-^b5.-F9ql__K?~4dK">
                                                                            <value name="TEXT">
                                                                              <shadow type="text" id="EIF6Od$(~J7~joTCW5tt">
                                                                                <field name="TEXT">final sell</field>
                                                                              </shadow>
                                                                            </value>
                                                                            <next>
                                                                              <block type="text_statement" id="F*,.Wq$91G*9lXZ.eAM]">
                                                                                <value name="TEXT">
                                                                                  <shadow type="text" id="|/y)wfIJS,xerd;pYt{8">
                                                                                    <field name="TEXT">abc</field>
                                                                                  </shadow>
                                                                                  <block type="variables_get" id="aq`].o%3zfRERhp9P1Z:">
                                                                                    <field name="VAR" id="?6{q@1dMn1rUO}Wdpo%a">final_sell</field>
                                                                                  </block>
                                                                                </value>
                                                                              </block>
                                                                            </next>
                                                                          </block>
                                                                        </statement>
                                                                        <next>
                                                                          <block type="notify" id="^Qc]E83,nhXX|HsGN*u[">
                                                                            <field name="NOTIFICATION_TYPE">info</field>
                                                                            <field name="NOTIFICATION_SOUND">silent</field>
                                                                            <value name="MESSAGE">
                                                                              <shadow type="text" id="o0.Z4WCVN1@V~Lkkv9nf">
                                                                                <field name="TEXT">abc</field>
                                                                              </shadow>
                                                                              <block type="variables_get" id="IW)uX/+k_]@dJVVx|QP9">
                                                                                <field name="VAR" id="U_|ZtI3=Zjv=JdeDgwf2">text_3</field>
                                                                              </block>
                                                                            </value>
                                                                            <next>
                                                                              <block type="purchase" id="ZyD^llwx#fjo{e:?hc#|">
                                                                                <field name="PURCHASE_LIST">PUT</field>
                                                                              </block>
                                                                            </next>
                                                                          </block>
                                                                        </next>
                                                                      </block>
                                                                    </statement>
                                                                  </block>
                                                                </next>
                                                              </block>
                                                            </next>
                                                          </block>
                                                        </next>
                                                      </block>
                                                    </next>
                                                  </block>
                                                </next>
                                              </block>
                                            </next>
                                          </block>
                                        </next>
                                      </block>
                                    </next>
                                  </block>
                                </next>
                              </block>
                            </next>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </next>
      </block>
    </statement>
  </block>
  <block type="logic_operation" id="0}B[8_0[-7DXhVoc`QyJ" disabled="true" x="0" y="4704">
    <field name="OP">AND</field>
  </block>
  <block type="logic_operation" id="uW(IKoo)J(Q.#=8b$j]!" disabled="true" x="0" y="4794">
    <field name="OP">AND</field>
  </block>
  <block type="variables_get" id="~[YZap-7xp?n[uguxjSj" disabled="true" x="0" y="4884">
    <field name="VAR" id="u]@6qd1s}n-P%#SW23iZ">sma_mid</field>
  </block>
  <block type="variables_get" id="#H.3Dj.^wOl+ty{TW%!!" disabled="true" x="0" y="4972">
    <field name="VAR" id="u]@6qd1s}n-P%#SW23iZ">sma_mid</field>
  </block>
</xml>
