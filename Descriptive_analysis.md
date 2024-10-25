**Incidence - SEER Research Plus Specialized Data (with county in case
listing), 17 Registries (excluding Alaska), November 2023 Submission
(2000-2021)**

### Eligibility

-   Known age &gt; 18 y/o
-   Site recode ICD-O-3 2023 Revision = Lung and bronchus
-   Malignant behavior
-   Baseline with no other cancers
-   Exclude missing information

### All the variables available

    ls(mydata)

    ##   [1] "Adjusted.CS.site.specific.factor.7..2004.2017.varying.by.schema."              
    ##   [2] "AFP.Post.Orchiectomy.Lab.Value.Recode..2010.."                                 
    ##   [3] "AFP.Pretreatment.Interpretation.Recode..2010.."                                
    ##   [4] "Age.recode.with..1.year.olds"                                                  
    ##   [5] "Age.recode.with..1.year.olds.and.90."                                          
    ##   [6] "Age.recode.with.single.ages.and.85."                                           
    ##   [7] "Age.recode.with.single.ages.and.90."                                           
    ##   [8] "AJCC.ID..2018.."                                                               
    ##   [9] "AJCC.stage.3rd.edition..1988.2003."                                            
    ##  [10] "AYA.site.recode.2020.Revision"                                                 
    ##  [11] "B.Symptoms.Recode..2010.."                                                     
    ##  [12] "Behavior.code.ICD.O.3"                                                         
    ##  [13] "Behavior.recode.for.analysis"                                                  
    ##  [14] "Brain.Molecular.Markers..2018.."                                               
    ##  [15] "Breast...Adjusted.AJCC.6th.M..1988.2015."                                      
    ##  [16] "Breast...Adjusted.AJCC.6th.N..1988.2015."                                      
    ##  [17] "Breast...Adjusted.AJCC.6th.Stage..1988.2015."                                  
    ##  [18] "Breast...Adjusted.AJCC.6th.T..1988.2015."                                      
    ##  [19] "Breast.Subtype..2010.."                                                        
    ##  [20] "Breslow.Thickness.Recode..2010.."                                              
    ##  [21] "CA.125.Pretreatment.Interpretation.Recode..2010.."                             
    ##  [22] "CEA.Pretreatment.Interpretation.Recode..2010.."                                
    ##  [23] "Chemotherapy.recode..yes..no.unk."                                             
    ##  [24] "Chromosome.19q..Loss.of.Heterozygosity..LOH..Recode..2010.."                   
    ##  [25] "Chromosome.1p..Loss.of.Heterozygosity..LOH..Recode..2010.."                    
    ##  [26] "CoC.Accredited.Flag..2018.."                                                   
    ##  [27] "COD.to.site.rec.KM"                                                            
    ##  [28] "COD.to.site.recode"                                                            
    ##  [29] "COD.to.site.recode.ICD.O.3.2023.Revision"                                      
    ##  [30] "COD.to.site.recode.ICD.O.3.2023.Revision.Expanded..1999.."                     
    ##  [31] "Coding.system.EOD..1973.2003."                                                 
    ##  [32] "Combined.Summary.Stage..2004.."                                                
    ##  [33] "CS.extension..2004.2015."                                                      
    ##  [34] "CS.lymph.nodes..2004.2015."                                                    
    ##  [35] "CS.mets.at.dx..2004.2015."                                                     
    ##  [36] "CS.Mets.Eval..2004.2015."                                                      
    ##  [37] "CS.Reg.Node.Eval..2004.2015."                                                  
    ##  [38] "CS.Schema...AJCC.6th.Edition"                                                  
    ##  [39] "CS.site.specific.factor.1..2004.2017.varying.by.schema."                       
    ##  [40] "CS.site.specific.factor.10..2004.2017.varying.by.schema."                      
    ##  [41] "CS.site.specific.factor.11..2004.2017.varying.by.schema."                      
    ##  [42] "CS.site.specific.factor.12..2004.2017.varying.by.schema."                      
    ##  [43] "CS.site.specific.factor.13..2004.2017.varying.by.schema."                      
    ##  [44] "CS.site.specific.factor.15..2004.2017.varying.by.schema."                      
    ##  [45] "CS.site.specific.factor.16..2004.2017.varying.by.schema."                      
    ##  [46] "CS.site.specific.factor.2..2004.2017.varying.by.schema."                       
    ##  [47] "CS.site.specific.factor.25..2004.2017.varying.by.schema."                      
    ##  [48] "CS.site.specific.factor.3..2004.2017.varying.by.schema."                       
    ##  [49] "CS.site.specific.factor.4..2004.2017.varying.by.schema."                       
    ##  [50] "CS.site.specific.factor.5..2004.2017.varying.by.schema."                       
    ##  [51] "CS.site.specific.factor.6..2004.2017.varying.by.schema."                       
    ##  [52] "CS.site.specific.factor.8..2004.2017.varying.by.schema."                       
    ##  [53] "CS.site.specific.factor.9..2004.2017.varying.by.schema."                       
    ##  [54] "CS.tumor.size..2004.2015."                                                     
    ##  [55] "CS.Tumor.Size.Ext.Eval..2004.2015."                                            
    ##  [56] "CS.version.derived..2004.2015."                                                
    ##  [57] "CS.version.input.current..2004.2015."                                          
    ##  [58] "CS.version.input.original..2004.2015."                                         
    ##  [59] "Cumulative.Expected..Calculated."                                              
    ##  [60] "Derived.AJCC.M..6th.ed..2004.2015."                                            
    ##  [61] "Derived.AJCC.M..7th.ed..2010.2015."                                            
    ##  [62] "Derived.AJCC.N..6th.ed..2004.2015."                                            
    ##  [63] "Derived.AJCC.N..7th.ed..2010.2015."                                            
    ##  [64] "Derived.AJCC.Stage.Group..6th.ed..2004.2015."                                  
    ##  [65] "Derived.AJCC.Stage.Group..7th.ed..2010.2015."                                  
    ##  [66] "Derived.AJCC.T..6th.ed..2004.2015."                                            
    ##  [67] "Derived.AJCC.T..7th.ed..2010.2015."                                            
    ##  [68] "Derived.EOD.2018.M..2018.."                                                    
    ##  [69] "Derived.EOD.2018.N..2018.."                                                    
    ##  [70] "Derived.EOD.2018.Stage.Group..2018.."                                          
    ##  [71] "Derived.EOD.2018.T..2018.."                                                    
    ##  [72] "Derived.HER2.Recode..2010.."                                                   
    ##  [73] "Derived.SEER.Cmb.Stg.Grp..2016.2017."                                          
    ##  [74] "Derived.SEER.Combined.M..2016.2017."                                           
    ##  [75] "Derived.SEER.Combined.M.Src..2016.2017."                                       
    ##  [76] "Derived.SEER.Combined.N..2016.2017."                                           
    ##  [77] "Derived.SEER.Combined.N.Src..2016.2017."                                       
    ##  [78] "Derived.SEER.Combined.T..2016.2017."                                           
    ##  [79] "Derived.SEER.Combined.T.Src..2016.2017."                                       
    ##  [80] "Derived.Summary.Grade.2018..2018.."                                            
    ##  [81] "Diagnostic.Confirmation"                                                       
    ##  [82] "End_date_field"                                                                
    ##  [83] "End.Calc.Vital.Status..Adjusted."                                              
    ##  [84] "EOD.10...extent..1988.2003."                                                   
    ##  [85] "EOD.10...nodes..1988.2003."                                                    
    ##  [86] "EOD.10...Prostate.path.ext..1995.2003."                                        
    ##  [87] "EOD.10...size..1988.2003."                                                     
    ##  [88] "EOD.4...extent..1983.1987."                                                    
    ##  [89] "EOD.4...nodes..1983.1987."                                                     
    ##  [90] "EOD.4...size..1983.1987."                                                      
    ##  [91] "EOD.Mets..2018.."                                                              
    ##  [92] "EOD.Primary.Tumor..2018.."                                                     
    ##  [93] "EOD.Regional.Nodes..2018.."                                                    
    ##  [94] "EOD.Schema.ID.Recode..2010.."                                                  
    ##  [95] "ER.Status.Recode.Breast.Cancer..1990.."                                        
    ##  [96] "Expanded.EOD.1....CP53..1973.1982."                                            
    ##  [97] "Expanded.EOD.1.2....CP53.54..1973.1982."                                       
    ##  [98] "Expanded.EOD.10....CP62..1973.1982."                                           
    ##  [99] "Expanded.EOD.11....CP63..1973.1982."                                           
    ## [100] "Expanded.EOD.12....CP64..1973.1982."                                           
    ## [101] "Expanded.EOD.13....CP65..1973.1982."                                           
    ## [102] "Expanded.EOD.2....CP54..1973.1982."                                            
    ## [103] "Expanded.EOD.3....CP55..1973.1982."                                            
    ## [104] "Expanded.EOD.4....CP56..1973.1982."                                            
    ## [105] "Expanded.EOD.5....CP57..1973.1982."                                            
    ## [106] "Expanded.EOD.6....CP58..1973.1982."                                            
    ## [107] "Expanded.EOD.7....CP59..1973.1982."                                            
    ## [108] "Expanded.EOD.8....CP60..1973.1982."                                            
    ## [109] "Expanded.EOD.9....CP61..1973.1982."                                            
    ## [110] "Fibrosis.Score.Recode..2010.."                                                 
    ## [111] "Final.Interval.Expected..12.month."                                            
    ## [112] "Final.Interval.Year..Calculated."                                              
    ## [113] "FIPS_code"                                                                     
    ## [114] "First.malignant.primary.indicator"                                             
    ## [115] "Gestational.Trophoblastic.Prognostic.Scoring.Index.Recode..2010.."             
    ## [116] "Gleason.Patterns.Clinical.Recode..2010.."                                      
    ## [117] "Gleason.Patterns.Pathological.Recode..2010.."                                  
    ## [118] "Gleason.Score.Clinical.Recode..2010.."                                         
    ## [119] "Gleason.Score.Pathological.Recode..2010.."                                     
    ## [120] "Grade.Clinical..2018.."                                                        
    ## [121] "Grade.Pathological..2018.."                                                    
    ## [122] "Grade.Recode..thru.2017."                                                      
    ## [123] "hCG.Post.Orchiectomy.Range.Recode..2010.."                                     
    ## [124] "Histologic.Type.ICD.O.3"                                                       
    ## [125] "Histology.recode...broad.groupings"                                            
    ## [126] "ICCC.site.recode.3rd.edition.IARC.2017"                                        
    ## [127] "ICCC.site.recode.extended.3rd.edition.IARC.2017"                               
    ## [128] "ICD.O.3.Hist.behav"                                                            
    ## [129] "ICD.O.3.Hist.behav..malignant"                                                 
    ## [130] "ID"                                                                            
    ## [131] "IHS.Link"                                                                      
    ## [132] "Invasion.Beyond.Capsule.Recode..2010.."                                        
    ## [133] "Ipsilateral.Adrenal.Gland.Involvement.Recode..2010.."                          
    ## [134] "Laterality"                                                                    
    ## [135] "LDH.Post.Orchiectomy.Range.Recode..2010.."                                     
    ## [136] "LDH.Pretreatment.Level.Recode..2010.."                                         
    ## [137] "LN.Head.and.Neck.Levels.I.III.Recode..2010.."                                  
    ## [138] "LN.Head.and.Neck.Levels.IV.V.Recode..2010.."                                   
    ## [139] "LN.Head.and.Neck.Levels.VI.VII.Recode..2010.."                                 
    ## [140] "LN.Head.and.Neck.Other.Recode..2010.."                                         
    ## [141] "LN.Positive.Axillary.Level.I.II.Recode..2010.."                                
    ## [142] "Lymph.Node.Size.Recode..2010.."                                                
    ## [143] "Lymph.vascular.Invasion..2004..varying.by.schema."                             
    ## [144] "Lymphoid.neoplasm.recode.2021.Revision"                                        
    ## [145] "Lymphoma...Ann.Arbor.Stage..1983.2015."                                        
    ## [146] "M.value...based.on.AJCC.3rd..1988.2003."                                       
    ## [147] "Major.Vein.Involvement.Recode..2010.."                                         
    ## [148] "Marital.status.at.diagnosis"                                                   
    ## [149] "Measured.Basal.Diameter.Recode..2010.."                                        
    ## [150] "Measured.Thickness.Recode..2010.."                                             
    ## [151] "Mets.at.DX.Distant.LN..2016.."                                                 
    ## [152] "Mets.at.DX.Other..2016.."                                                      
    ## [153] "Mitotic.Rate.Melanoma.Recode..2010.."                                          
    ## [154] "N.value...based.on.AJCC.3rd..1988.2003."                                       
    ## [155] "Number.of.Cores.Examined.Recode..2010.."                                       
    ## [156] "Number.of.Cores.Positive.Recode..2010.."                                       
    ## [157] "Number.of.Examined.Para.Aortic.Nodes.Recode..2010.."                           
    ## [158] "Number.of.Examined.Pelvic.Nodes.Recode..2010.."                                
    ## [159] "Number.of.Intervals..Calculated."                                              
    ## [160] "Number.of.Positive.Para.Aortic.Nodes.Recode..2010.."                           
    ## [161] "Number.of.Positive.Pelvic.Nodes.Recode..2010.."                                
    ## [162] "Origin.recode.NHIA..Hispanic..Non.Hisp."                                       
    ## [163] "Patient.ID"                                                                    
    ## [164] "Perineural.Invasion.Recode..2010.."                                            
    ## [165] "Peripheral.Blood.Involvement.Recode..2010.."                                   
    ## [166] "Peritoneal.Cytology.Recode..2010.."                                            
    ## [167] "Pleural.Effusion.Recode..2010.."                                               
    ## [168] "PR.Status.Recode.Breast.Cancer..1990.."                                        
    ## [169] "PRCDA.2020"                                                                    
    ## [170] "PRCDA.Region"                                                                  
    ## [171] "Primary.by.international.rules"                                                
    ## [172] "Primary.Site"                                                                  
    ## [173] "Primary.Site...labeled"                                                        
    ## [174] "Prostate.Pathological.Extension..2018.."                                       
    ## [175] "PSA.Lab.Value.Recode..2010.."                                                  
    ## [176] "Race.and.origin.recode..NHW..NHB..NHAIAN..NHAPI..Hispanic."                    
    ## [177] "Race.ethnicity"                                                                
    ## [178] "Race.recode..W..B..AI..API."                                                   
    ## [179] "Race.recode..White..Black..Other."                                             
    ## [180] "Radiation.recode"                                                              
    ## [181] "Radiation.to.Brain.or.CNS.Recode..1988.1997."                                  
    ## [182] "Reason.no.cancer.directed.surgery"                                             
    ## [183] "Record.number.recode"                                                          
    ## [184] "Regional.nodes.examined..1988.."                                               
    ## [185] "Regional.nodes.positive..1988.."                                               
    ## [186] "Residual.Tumor.Volume.Post.Cytoreduction.Recode..2010.."                       
    ## [187] "Response.to.Neoadjuvant.Therapy.Recode..2010.."                                
    ## [188] "RX.Summ..Reg.LN.Examined..1998.2002."                                          
    ## [189] "RX.Summ..Scope.Reg.LN.Sur..2003.."                                             
    ## [190] "RX.Summ..Surg.Oth.Reg.Dis..2003.."                                             
    ## [191] "RX.Summ..Surg.Prim.Site..1998.."                                               
    ## [192] "RX.Summ..Surg.Rad.Seq"                                                         
    ## [193] "RX.Summ..Systemic.Sur.Seq..2007.."                                             
    ## [194] "Sarcomatoid.Features.Recode..2010.."                                           
    ## [195] "Schema.ID..2018.."                                                             
    ## [196] "Scope.of.reg.lymph.nd.surg..1998.2002."                                        
    ## [197] "SEER.Brain.and.CNS.Recode"                                                     
    ## [198] "SEER.cause.specific.death.classification"                                      
    ## [199] "SEER.Combined.Mets.at.DX.bone..2010.."                                         
    ## [200] "SEER.Combined.Mets.at.DX.brain..2010.."                                        
    ## [201] "SEER.Combined.Mets.at.DX.liver..2010.."                                        
    ## [202] "SEER.Combined.Mets.at.DX.lung..2010.."                                         
    ## [203] "SEER.Combined.Summary.Stage.2000..2004.2017."                                  
    ## [204] "SEER.historic.stage.A..1973.2015."                                             
    ## [205] "SEER.modified.AJCC.stage.3rd..1988.2003."                                      
    ## [206] "SEER.other.cause.of.death.classification"                                      
    ## [207] "SEER.registry"                                                                 
    ## [208] "SEER.registry..with.CA.and.GA.as.whole.states."                                
    ## [209] "Separate.Tumor.Nodules.Ipsilateral.Lung.Recode..2010.."                        
    ## [210] "Sequence.number"                                                               
    ## [211] "Sex"                                                                           
    ## [212] "Site...mal.ins..least.detail."                                                 
    ## [213] "Site...mal.ins..mid.detail."                                                   
    ## [214] "Site...mal.ins..most.detail."                                                  
    ## [215] "Site...malignant..least.detail."                                               
    ## [216] "Site...malignant..mid.detail."                                                 
    ## [217] "Site...malignant..most.detail."                                                
    ## [218] "Site.recode...rare.tumors"                                                     
    ## [219] "Site.recode.ICD.O.3.2023.Revision"                                             
    ## [220] "Site.recode.ICD.O.3.2023.Revision.Expanded"                                    
    ## [221] "Site.recode.ICD.O.3.WHO.2008"                                                  
    ## [222] "Site.recode.ICD.O.3.WHO.2008..for.SIRs."                                       
    ## [223] "Site.specific.surgery..1973.1997.varying.detail.by.year.and.site."             
    ## [224] "SS.seq.....mal..least.detail."                                                 
    ## [225] "SS.seq.....mal..mid.detail."                                                   
    ## [226] "SS.seq.....mal..most.detail."                                                  
    ## [227] "SS.seq.....mal.ins..least.detail."                                             
    ## [228] "SS.seq.....mal.ins..mid.detail."                                               
    ## [229] "SS.seq.....mal.ins..most.detail."                                              
    ## [230] "SS.seq...1975....mal..least.detail."                                           
    ## [231] "SS.seq...1975....mal..mid.detail."                                             
    ## [232] "SS.seq...1975....mal..most.detail."                                            
    ## [233] "SS.seq...1975....mal.ins..least.detail."                                       
    ## [234] "SS.seq...1975....mal.ins..mid.detail."                                         
    ## [235] "SS.seq...1975....mal.ins..most.detail."                                        
    ## [236] "SS.seq...1992....mal..least.detail."                                           
    ## [237] "SS.seq...1992....mal..mid.detail."                                             
    ## [238] "SS.seq...1992....mal..most.detail."                                            
    ## [239] "SS.seq...1992....mal.ins..least.detail."                                       
    ## [240] "SS.seq...1992....mal.ins..mid.detail."                                         
    ## [241] "SS.seq...1992....mal.ins..most.detail."                                        
    ## [242] "SS.seq...2000....mal..least.detail."                                           
    ## [243] "SS.seq...2000....mal..mid.detail."                                             
    ## [244] "SS.seq...2000....mal..most.detail."                                            
    ## [245] "SS.seq...2000....mal.ins..least.detail."                                       
    ## [246] "SS.seq...2000....mal.ins..mid.detail."                                         
    ## [247] "SS.seq...2000....mal.ins..most.detail."                                        
    ## [248] "Start_date_field"                                                              
    ## [249] "State.county"                                                                  
    ## [250] "Summary.stage.2000..1998.2017."                                                
    ## [251] "Surgery.of.oth.reg.dis.sites..1998.2002."                                      
    ## [252] "Survival.months"                                                               
    ## [253] "Survival.months.flag"                                                          
    ## [254] "T.value...based.on.AJCC.3rd..1988.2003."                                       
    ## [255] "Time.from.diagnosis.to.treatment.in.days.recode"                               
    ## [256] "TNM.7.CS.v0204..Schema..thru.2017."                                            
    ## [257] "TNM.7.CS.v0204..Schema.recode"                                                 
    ## [258] "TNM.Edition.Number..2016.2017."                                                
    ## [259] "Total.number.of.benign.borderline.tumors.for.patient"                          
    ## [260] "Total.number.of.in.situ.malignant.tumors.for.patient"                          
    ## [261] "Tumor.Deposits.Recode..2010.."                                                 
    ## [262] "Tumor.marker.1..1990.2003."                                                    
    ## [263] "Tumor.marker.2..1990.2003."                                                    
    ## [264] "Tumor.marker.3..1998.2003."                                                    
    ## [265] "Tumor.Size.Over.Time.Recode..1988.."                                           
    ## [266] "Tumor.Size.Summary..2016.."                                                    
    ## [267] "Type.of.Reporting.Source"                                                      
    ## [268] "Ulceration.Recode..2010.."                                                     
    ## [269] "Visceral.and.Parietal.Pleural.Invasion.Recode..2010.."                         
    ## [270] "Vital.status.recode..study.cutoff.used."                                       
    ## [271] "X..CRC.Test.Ever..age.50....sae.2004.2007."                                    
    ## [272] "X..CRC.Test.Ever..age.50....sae.2008.2010."                                    
    ## [273] "X..Current.Smoker..age.18....sae.1997.1999."                                   
    ## [274] "X..Current.Smoker..age.18....sae.2000.2003."                                   
    ## [275] "X..Current.Smoker..age.18....sae.2004.2007."                                   
    ## [276] "X..Current.Smoker..age.18....sae.2008.2010."                                   
    ## [277] "X..Current.Smoker..age.18....sae.2011.2013."                                   
    ## [278] "X..Current.Smoker..age.18....sae.2014.2016."                                   
    ## [279] "X..Current.Smoker..females.age.18....sae.1997.1999."                           
    ## [280] "X..Current.Smoker..females.age.18....sae.2000.2003."                           
    ## [281] "X..Current.Smoker..females.age.18....sae.2004.2007."                           
    ## [282] "X..Current.Smoker..females.age.18....sae.2008.2010."                           
    ## [283] "X..Current.Smoker..females.age.18....sae.2011.2013."                           
    ## [284] "X..Current.Smoker..females.age.18....sae.2014.2016."                           
    ## [285] "X..Current.Smoker..males.age.18....sae.1997.1999."                             
    ## [286] "X..Current.Smoker..males.age.18....sae.2000.2003."                             
    ## [287] "X..Current.Smoker..males.age.18....sae.2004.2007."                             
    ## [288] "X..Current.Smoker..males.age.18....sae.2008.2010."                             
    ## [289] "X..Current.Smoker..males.age.18....sae.2011.2013."                             
    ## [290] "X..Current.Smoker..males.age.18....sae.2014.2016."                             
    ## [291] "X..Endoscopy.Ever..age.50....sae.2004.2007."                                   
    ## [292] "X..Endoscopy.Ever..age.50....sae.2008.2010."                                   
    ## [293] "X..Ever.Smoker..age.18....sae.1997.1999."                                      
    ## [294] "X..Ever.Smoker..age.18....sae.2000.2003."                                      
    ## [295] "X..Ever.Smoker..age.18....sae.2004.2007."                                      
    ## [296] "X..Ever.Smoker..age.18....sae.2008.2010."                                      
    ## [297] "X..Ever.Smoker..females.age.18....sae.1997.1999."                              
    ## [298] "X..Ever.Smoker..females.age.18....sae.2000.2003."                              
    ## [299] "X..Ever.Smoker..females.age.18....sae.2004.2007."                              
    ## [300] "X..Ever.Smoker..females.age.18....sae.2008.2010."                              
    ## [301] "X..Ever.Smoker..males.age.18....sae.1997.1999."                                
    ## [302] "X..Ever.Smoker..males.age.18....sae.2000.2003."                                
    ## [303] "X..Ever.Smoker..males.age.18....sae.2004.2007."                                
    ## [304] "X..Ever.Smoker..males.age.18....sae.2008.2010."                                
    ## [305] "X..FOBT.Ever..age.50....sae.2004.2007."                                        
    ## [306] "X..FOBT.Ever..age.50....sae.2008.2010."                                        
    ## [307] "X..Former.Smoker..age.18....sae.2011.2013."                                    
    ## [308] "X..Former.Smoker..age.18....sae.2014.2016."                                    
    ## [309] "X..Former.Smoker..females.age.18....sae.2011.2013."                            
    ## [310] "X..Former.Smoker..females.age.18....sae.2014.2016."                            
    ## [311] "X..Former.Smoker..males.age.18....sae.2011.2013."                              
    ## [312] "X..Former.Smoker..males.age.18....sae.2014.2016."                              
    ## [313] "X..Long.term.former.smoker.quitting...1.year..age.18....sae.2011.2013."        
    ## [314] "X..Long.term.former.smoker.quitting...1.year..age.18....sae.2014.2016."        
    ## [315] "X..Long.term.former.smoker.quitting...1.year..females.age.18....sae.2011.2013."
    ## [316] "X..Long.term.former.smoker.quitting...1.year..females.age.18....sae.2014.2016."
    ## [317] "X..Long.term.former.smoker.quitting...1.year..males.age.18....sae.2011.2013."  
    ## [318] "X..Long.term.former.smoker.quitting...1.year..males.age.18....sae.2014.2016."  
    ## [319] "X..Mammography.within.2.years..age.40....sae.1997.1999."                       
    ## [320] "X..Mammography.within.2.years..age.40....sae.2000.2003."                       
    ## [321] "X..Mammography.within.2.years..age.40....sae.2004.2007."                       
    ## [322] "X..Mammography.within.2.years..age.40....sae.2008.2010."                       
    ## [323] "X..Mammography.within.2.years..age.40....sae.2011.2016."                       
    ## [324] "X..Mammography.within.2.years..age.50.74...sae.2011.2016."                     
    ## [325] "X..Pap.Smear.within.3.years..age.18....sae.1997.1999."                         
    ## [326] "X..Pap.Smear.within.3.years..age.18....sae.2000.2003."                         
    ## [327] "X..Pap.Smear.within.3.years..age.18....sae.2004.2007."                         
    ## [328] "X..Pap.Smear.within.3.years..age.18....sae.2008.2010."                         
    ## [329] "X..Pap.Smear.within.3.years..age.18....sae.2011.2016."                         
    ## [330] "X2.Digit.NS.EOD.part.1..1973.1982."                                            
    ## [331] "X2.Digit.NS.EOD.part.2..1973.1982."                                            
    ## [332] "X2.Digit.SS.EOD.part.1..1973.1982."                                            
    ## [333] "X2.Digit.SS.EOD.part.2..1973.1982."                                            
    ## [334] "X7th.Edition.Stage.Group.Recode..2016.2017."                                   
    ## [335] "Year.of.death.recode"                                                          
    ## [336] "Year.of.diagnosis"                                                             
    ## [337] "Year.of.follow.up.recode"

### Case numbers

    nrow(mydata)

    ## [1] 703003

### Variables pulled and prepped

    mydata_1 <- mydata %>% select(Patient.ID, Sex, Year.of.diagnosis, Year.of.follow.up.recode, Year.of.death.recode, Age.recode.with.single.ages.and.90., Marital.status.at.diagnosis, Race.and.origin.recode..NHW..NHB..NHAIAN..NHAPI..Hispanic., Histologic.Type.ICD.O.3, Laterality, SEER.modified.AJCC.stage.3rd..1988.2003., Derived.AJCC.Stage.Group..6th.ed..2004.2015., Derived.SEER.Cmb.Stg.Grp..2016.2017., Derived.EOD.2018.Stage.Group..2018.., Combined.Summary.Stage..2004.., Summary.stage.2000..1998.2017., Sequence.number, Chemotherapy.recode..yes..no.unk., Radiation.recode, Reason.no.cancer.directed.surgery, Time.from.diagnosis.to.treatment.in.days.recode, Vital.status.recode..study.cutoff.used., Race.recode..White..Black..Other., Survival.months, SEER.other.cause.of.death.classification, SEER.cause.specific.death.classification, COD.to.site.recode.ICD.O.3.2023.Revision.Expanded..1999.., State.county, X..Current.Smoker..age.18....sae.2000.2003., X..Current.Smoker..age.18....sae.2004.2007., X..Current.Smoker..age.18....sae.2008.2010., X..Current.Smoker..age.18....sae.2011.2013., X..Current.Smoker..age.18....sae.2014.2016.)

    ls(mydata_1)

    ##  [1] "Age.recode.with.single.ages.and.90."                       
    ##  [2] "Chemotherapy.recode..yes..no.unk."                         
    ##  [3] "COD.to.site.recode.ICD.O.3.2023.Revision.Expanded..1999.." 
    ##  [4] "Combined.Summary.Stage..2004.."                            
    ##  [5] "Derived.AJCC.Stage.Group..6th.ed..2004.2015."              
    ##  [6] "Derived.EOD.2018.Stage.Group..2018.."                      
    ##  [7] "Derived.SEER.Cmb.Stg.Grp..2016.2017."                      
    ##  [8] "Histologic.Type.ICD.O.3"                                   
    ##  [9] "Laterality"                                                
    ## [10] "Marital.status.at.diagnosis"                               
    ## [11] "Patient.ID"                                                
    ## [12] "Race.and.origin.recode..NHW..NHB..NHAIAN..NHAPI..Hispanic."
    ## [13] "Race.recode..White..Black..Other."                         
    ## [14] "Radiation.recode"                                          
    ## [15] "Reason.no.cancer.directed.surgery"                         
    ## [16] "SEER.cause.specific.death.classification"                  
    ## [17] "SEER.modified.AJCC.stage.3rd..1988.2003."                  
    ## [18] "SEER.other.cause.of.death.classification"                  
    ## [19] "Sequence.number"                                           
    ## [20] "Sex"                                                       
    ## [21] "State.county"                                              
    ## [22] "Summary.stage.2000..1998.2017."                            
    ## [23] "Survival.months"                                           
    ## [24] "Time.from.diagnosis.to.treatment.in.days.recode"           
    ## [25] "Vital.status.recode..study.cutoff.used."                   
    ## [26] "X..Current.Smoker..age.18....sae.2000.2003."               
    ## [27] "X..Current.Smoker..age.18....sae.2004.2007."               
    ## [28] "X..Current.Smoker..age.18....sae.2008.2010."               
    ## [29] "X..Current.Smoker..age.18....sae.2011.2013."               
    ## [30] "X..Current.Smoker..age.18....sae.2014.2016."               
    ## [31] "Year.of.death.recode"                                      
    ## [32] "Year.of.diagnosis"                                         
    ## [33] "Year.of.follow.up.recode"

### Demographics

#### Age at diagnosis (Continuous)

    # Transform the "age" column to extract the numeric part
    mydata_1 <- mydata_1 %>%
      mutate(age = as.numeric(gsub("[^0-9]", "", Age.recode.with.single.ages.and.90.)))

    summary(mydata_1$age)  # Gives Min, 1st Qu., Median, Mean, 3rd Qu., Max

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   19.00   61.00   68.00   67.89   76.00   90.00

    sd(mydata_1$age)       # Standard Deviation

    ## [1] 10.89303

    # Create a histogram of the age column
    ggplot(mydata_1, aes(x = age)) +
      geom_histogram(binwidth = 3, fill = "lightblue", color = "black") +
      scale_x_continuous(breaks = seq(10, 100, by = 5)) +
      xlab("Age") +
      ylab("Cases") +
      ggtitle("Age distribution")

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-56-1.png)

#### Sex (Categorical)

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(Sex) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">Sex</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Female</td>
<td style="text-align: right;">329770</td>
<td style="text-align: right;">46.9</td>
</tr>
<tr class="even">
<td style="text-align: left;">Male</td>
<td style="text-align: right;">373233</td>
<td style="text-align: right;">53.1</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(Sex) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = Sex)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.4, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Sex", x = "", y = "Counts (*1000)") +
      scale_y_continuous(limits = c(0, 375)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(
        axis.text.x = element_text(angle = 0, hjust = 1)  # Angle x-axis labels
      ) +
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-57-1.png)

#### Marital status at diagnosis (Categorical)

    # Convert category to a factor and specify the order
    mydata_1$Marital.status.at.diagnosis <- factor(mydata_1$Marital.status.at.diagnosis, levels = c("Single (never married)", "Widowed", "Divorced", "Separated", "Married (including common law)", "Unknown"))

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(Marital.status.at.diagnosis) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">Marital.status.at.diagnosis</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Single (never married)</td>
<td style="text-align: right;">99231</td>
<td style="text-align: right;">14.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Widowed</td>
<td style="text-align: right;">120649</td>
<td style="text-align: right;">17.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Divorced</td>
<td style="text-align: right;">85811</td>
<td style="text-align: right;">12.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">Separated</td>
<td style="text-align: right;">8343</td>
<td style="text-align: right;">1.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Married (including common law)</td>
<td style="text-align: right;">358558</td>
<td style="text-align: right;">51.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Unknown</td>
<td style="text-align: right;">28815</td>
<td style="text-align: right;">4.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NA</td>
<td style="text-align: right;">1596</td>
<td style="text-align: right;">0.2</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(Marital.status.at.diagnosis) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = Marital.status.at.diagnosis)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.7, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Marital status at diagnosis", x = "", y = "Counts (*1000)") +
      scale_y_continuous(limits = c(0, 375)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(
        axis.text.x = element_text(angle = 25, hjust = 1)  # Angle x-axis labels
      ) +
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-58-1.png)

#### Race and origin 1 (Categorical)

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(Race.and.origin.recode..NHW..NHB..NHAIAN..NHAPI..Hispanic.) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<colgroup>
<col style="width: 76%" />
<col style="width: 9%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th
style="text-align: left;">Race.and.origin.recode..NHW..NHB..NHAIAN..NHAPI..Hispanic.</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Hispanic (All Races)</td>
<td style="text-align: right;">44516</td>
<td style="text-align: right;">6.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">Non-Hispanic American Indian/Alaska
Native</td>
<td style="text-align: right;">2707</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Non-Hispanic Asian or Pacific
Islander</td>
<td style="text-align: right;">48884</td>
<td style="text-align: right;">7.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Non-Hispanic Black</td>
<td style="text-align: right;">75449</td>
<td style="text-align: right;">10.7</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Non-Hispanic Unknown Race</td>
<td style="text-align: right;">1076</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">Non-Hispanic White</td>
<td style="text-align: right;">530371</td>
<td style="text-align: right;">75.4</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(Race.and.origin.recode..NHW..NHB..NHAIAN..NHAPI..Hispanic.) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = Race.and.origin.recode..NHW..NHB..NHAIAN..NHAPI..Hispanic.)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.5, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Race and origin", x = "", y = "Counts (*1000)") +
      scale_y_continuous(limits = c(0, 600)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(
        axis.text.x = element_text(angle = 25, hjust = 1)  # Angle x-axis labels
      ) +
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-59-1.png)

#### Race and origin 2 (Categorical)

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(Race.recode..White..Black..Other.) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<colgroup>
<col style="width: 76%" />
<col style="width: 9%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Race.recode..White..Black..Other.</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Black</td>
<td style="text-align: right;">76221</td>
<td style="text-align: right;">10.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">Other (American Indian/AK Native,
Asian/Pacific Islander)</td>
<td style="text-align: right;">52391</td>
<td style="text-align: right;">7.5</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Unknown</td>
<td style="text-align: right;">1566</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">White</td>
<td style="text-align: right;">572825</td>
<td style="text-align: right;">81.5</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(Race.recode..White..Black..Other.) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = Race.recode..White..Black..Other.)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.5, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Race and origin", x = "", y = "Counts (*1000)") +
      scale_y_continuous(limits = c(0, 600)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(
        axis.text.x = element_text(angle = 25, hjust = 1)  # Angle x-axis labels
      ) +
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-60-1.png)

### Tumor characteristics

#### Histological type

Categorized based on ICD code: Lewis DR, Check DP, Caporaso NE, Travis
WD, Devesa SS. US lung cancer trends by histologic type. Cancer. 2014
Sep 15;120(18):2883-92. doi: 10.1002/cncr.28749. Epub 2014 Aug 11. PMID:
25113306; PMCID: PMC4187244.

    #Categorical variable
    mydata_1 <- mydata_1 %>%
      mutate(histological_type = case_when(
        Histologic.Type.ICD.O.3 %in% c(8051:8052, 8070:8076, 8078, 8083:8084, 8090, 8094, 8120, 8123) ~ "Squamous Cell Carcinoma",
        Histologic.Type.ICD.O.3 %in% c(8002, 8041:8045) ~ "Small Cell Carcinoma",
        Histologic.Type.ICD.O.3 %in% c(8015, 8050, 8140:8141, 8143:8145, 8147, 8190, 8201, 8211, 
                                       8250:8255, 8260, 8290, 8310, 8320, 8323, 8333, 8401, 
                                       8440, 8470:8471, 8480:8481, 8490, 8503, 8507, 8550, 
                                       8570:8572, 8574, 8576) ~ "Adenocarcinoma",
        Histologic.Type.ICD.O.3 %in% c(8012:8014, 8021, 8034, 8082) ~ "Large Cell Carcinoma",
        Histologic.Type.ICD.O.3 %in% c(8003:8004, 8022, 8030:8035, 8200, 8240:8241, 8243:8246, 
                                       8249, 8430, 8525, 8560, 8562, 8575) ~ "Other Specified Carcinoma",
        Histologic.Type.ICD.O.3 %in% c(8010:8011, 8020, 8230, 8046, 8000:8001) ~ "Unspecified Malignant Neoplasms",
        Histologic.Type.ICD.O.3 %in% c(8580:9999, 8005, 8095, 8124, 8130, 8146, 8160, 8170, 
                                       8231, 8247, 8263, 8312, 8340:8341, 8350, 8370, 8441, 
                                       8460, 8500, 8501, 8510, 8524, 8530, 8551) ~ "Omitted Cases (non-carcinoma or metastasis)",
        TRUE ~ "Other"  # Default case for any unmatched codes
      ))

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(histological_type) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">histological_type</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Adenocarcinoma</td>
<td style="text-align: right;">292676</td>
<td style="text-align: right;">41.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">Large Cell Carcinoma</td>
<td style="text-align: right;">18040</td>
<td style="text-align: right;">2.6</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Omitted Cases (non-carcinoma or
metastasis)</td>
<td style="text-align: right;">7753</td>
<td style="text-align: right;">1.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Other</td>
<td style="text-align: right;">514</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Other Specified Carcinoma</td>
<td style="text-align: right;">33298</td>
<td style="text-align: right;">4.7</td>
</tr>
<tr class="even">
<td style="text-align: left;">Small Cell Carcinoma</td>
<td style="text-align: right;">99104</td>
<td style="text-align: right;">14.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Squamous Cell Carcinoma</td>
<td style="text-align: right;">149641</td>
<td style="text-align: right;">21.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">Unspecified Malignant Neoplasms</td>
<td style="text-align: right;">101977</td>
<td style="text-align: right;">14.5</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(histological_type) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = histological_type)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.7, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Histological type", y = "Counts (*1000)", x = "") +
      scale_y_continuous(limits = c(0, 310)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(
        axis.text.x = element_text(angle = 25, hjust = 1)  # Angle x-axis labels
      ) +
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-61-1.png)

#### Laterality (Categorical)

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(Laterality) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<colgroup>
<col style="width: 75%" />
<col style="width: 9%" />
<col style="width: 15%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Laterality</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Bilateral, single primary</td>
<td style="text-align: right;">8843</td>
<td style="text-align: right;">1.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">Left - origin of primary</td>
<td style="text-align: right;">275296</td>
<td style="text-align: right;">39.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Not a paired site</td>
<td style="text-align: right;">605</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Only one side - side unspecified</td>
<td style="text-align: right;">2838</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Paired site, but no information concerning
laterality</td>
<td style="text-align: right;">24579</td>
<td style="text-align: right;">3.5</td>
</tr>
<tr class="even">
<td style="text-align: left;">Right - origin of primary</td>
<td style="text-align: right;">390842</td>
<td style="text-align: right;">55.6</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(Laterality) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = Laterality)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.5, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Laterality", x = "", y = "Counts (*1000)") +
      scale_y_continuous(limits = c(0, 450)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(
        axis.text.x = element_text(angle = 25, hjust = 1)  # Angle x-axis labels
      ) +
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-62-1.png)

#### Clinical stage (Categorical)

    stage00_03 <- mydata_1 %>% filter(Year.of.diagnosis %in% c(2000:2003)) %>% 
      mutate(stage = case_when(
        SEER.modified.AJCC.stage.3rd..1988.2003. == 10 ~ "I",
        SEER.modified.AJCC.stage.3rd..1988.2003. == 20 ~ "II",
        SEER.modified.AJCC.stage.3rd..1988.2003. == 31 ~ "IIIA",
        SEER.modified.AJCC.stage.3rd..1988.2003. == 32 ~ "IIIB",
        SEER.modified.AJCC.stage.3rd..1988.2003. == 40 ~ "IV",
        TRUE ~ "Missing"  # Default case for any unmatched codes
      ))

    stage04_15 <- mydata_1 %>% filter(Year.of.diagnosis %in% c(2004:2015)) %>% 
      mutate(stage = case_when(
        Derived.AJCC.Stage.Group..6th.ed..2004.2015. == "IA" ~ "IA",
        Derived.AJCC.Stage.Group..6th.ed..2004.2015. == "IB" ~ "IB",
        Derived.AJCC.Stage.Group..6th.ed..2004.2015. == "IIA" ~ "IIA",
        Derived.AJCC.Stage.Group..6th.ed..2004.2015. == "IIB" ~ "IIB",
        Derived.AJCC.Stage.Group..6th.ed..2004.2015. == "IIIA" ~ "IIIA",
        Derived.AJCC.Stage.Group..6th.ed..2004.2015. == "IIIB" ~ "IIIB",
        Derived.AJCC.Stage.Group..6th.ed..2004.2015. == "IV" ~ "IV",
        TRUE ~ "Missing"  # Default case for any unmatched codes
      ))

    stage16_17 <- mydata_1 %>% filter(Year.of.diagnosis %in% c(2016:2017)) %>% 
      mutate(stage = case_when(
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "0" ~ "I",
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "1A" ~ "IA",
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "1B" ~ "IB",
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "2" ~ "II",
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "2A" ~ "IIA",
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "2B" ~ "IIB",
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "3" ~ "III",
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "3A" ~ "IIIA",
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "3B" ~ "IIIB",
        Derived.SEER.Cmb.Stg.Grp..2016.2017. == "4" ~ "IV",
        TRUE ~ "Missing"  # Default case for any unmatched codes
      ))

    stage18_21 <- mydata_1 %>% filter(Year.of.diagnosis %in% c(2018:2021)) %>% 
      mutate(stage = case_when(
        Derived.EOD.2018.Stage.Group..2018.. == "0" ~ "I",
        Derived.EOD.2018.Stage.Group..2018.. == "1A1" ~ "IA",
        Derived.EOD.2018.Stage.Group..2018.. == "1B2" ~ "IB",
        Derived.EOD.2018.Stage.Group..2018.. == "1A3" ~ "II",
        Derived.EOD.2018.Stage.Group..2018.. == "1B" ~ "IIA",
        Derived.EOD.2018.Stage.Group..2018.. == "2A" ~ "IIB",
        Derived.EOD.2018.Stage.Group..2018.. == "2B" ~ "III",
        Derived.EOD.2018.Stage.Group..2018.. == "3" ~ "IIIA",
        Derived.EOD.2018.Stage.Group..2018.. == "3A" ~ "IIIB",
        Derived.EOD.2018.Stage.Group..2018.. == "3B" ~ "IV",
        Derived.EOD.2018.Stage.Group..2018.. == "3C" ~ "IV",
        Derived.EOD.2018.Stage.Group..2018.. == "4" ~ "IV",
        Derived.EOD.2018.Stage.Group..2018.. == "4A" ~ "IVA",
        Derived.EOD.2018.Stage.Group..2018.. == "4B" ~ "IVB",
        TRUE ~ "Missing"  # Default case for any unmatched codes
      ))

    mydata_1 <- stage00_03 %>% full_join(stage04_15, by = "Patient.ID") %>% 
      full_join(stage16_17, by = "Patient.ID") %>% 
      full_join(stage18_21, by = "Patient.ID") %>% mutate(final_stage = case_when(
        !is.na(stage.x) & is.na(stage.y) & is.na(stage.x.x) & is.na(stage.y.y) ~ stage.x,
        is.na(stage.x) & !is.na(stage.y) & is.na(stage.x.x) & is.na(stage.y.y) ~ stage.y,
        is.na(stage.x) & is.na(stage.y) & !is.na(stage.x.x) & is.na(stage.y.y) ~ stage.x.x,
        is.na(stage.x) & is.na(stage.y) & is.na(stage.x.x) & !is.na(stage.y.y) ~ stage.y.y,
        is.na(stage.x) & is.na(stage.y) & is.na(stage.x.x) & is.na(stage.y.y) ~ NA_character_,
      )) %>% select(Patient.ID, final_stage) %>% full_join(mydata_1, by = "Patient.ID")

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(final_stage) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">final_stage</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">I</td>
<td style="text-align: right;">24928</td>
<td style="text-align: right;">3.5</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA</td>
<td style="text-align: right;">49979</td>
<td style="text-align: right;">7.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IB</td>
<td style="text-align: right;">36836</td>
<td style="text-align: right;">5.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">II</td>
<td style="text-align: right;">10277</td>
<td style="text-align: right;">1.5</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IIA</td>
<td style="text-align: right;">12511</td>
<td style="text-align: right;">1.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">IIB</td>
<td style="text-align: right;">17067</td>
<td style="text-align: right;">2.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">III</td>
<td style="text-align: right;">7088</td>
<td style="text-align: right;">1.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IIIA</td>
<td style="text-align: right;">58079</td>
<td style="text-align: right;">8.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IIIB</td>
<td style="text-align: right;">99279</td>
<td style="text-align: right;">14.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IV</td>
<td style="text-align: right;">276974</td>
<td style="text-align: right;">39.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IVA</td>
<td style="text-align: right;">23059</td>
<td style="text-align: right;">3.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">IVB</td>
<td style="text-align: right;">29428</td>
<td style="text-align: right;">4.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Missing</td>
<td style="text-align: right;">57498</td>
<td style="text-align: right;">8.2</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(final_stage) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = final_stage)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.7, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Clinical stage at diagnosis", y = "Counts (*1000)", x = "") +
      scale_y_continuous(limits = c(0, 300)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-63-1.png)

#### Clinical stage summary (Categorical)

    mydata_1 <- mydata_1 %>% 
      mutate(combined_stage = case_when(
        Year.of.diagnosis < 2004 ~ Summary.stage.2000..1998.2017.,  # Use stage_A if year <= 2004
        Year.of.diagnosis >= 2004 ~ Combined.Summary.Stage..2004..    # Use stage_B if year > 2004
      ))

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(combined_stage) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">combined_stage</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Distant</td>
<td style="text-align: right;">394995</td>
<td style="text-align: right;">56.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">In situ</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Localized</td>
<td style="text-align: right;">125192</td>
<td style="text-align: right;">17.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">Regional</td>
<td style="text-align: right;">161925</td>
<td style="text-align: right;">23.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Unknown/unstaged</td>
<td style="text-align: right;">20888</td>
<td style="text-align: right;">3.0</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(combined_stage) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = combined_stage)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.7, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Clinical stage at diagnosis", y = "Counts (*1000)", x = "") +
      scale_y_continuous(limits = c(0, 400)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-64-1.png)

#### Stage I-IIIA vs. IIIB-IV and Before/After 2015

    # Stratify by stage I-IIIA vs. IIIB-IV and Before/After 2015
    mydata_1 <- mydata_1 %>% filter(final_stage != "Missing") %>% 
      mutate(stage_binary = case_when(
        final_stage %in% c("I", "IA", "IB", "II", "IIA", "IIB", "III", "IIIA") ~ "Early stage",
        final_stage %in% c("IIIB", "IV", "IVA", "IVB") ~ "Late stage"
      )) %>% 
      mutate(year_2015 = case_when(
        Year.of.diagnosis < 2015 ~ "Before 2015",
        Year.of.diagnosis >= 2015 ~ "After 2015"
      )) %>% select(Patient.ID, stage_binary, year_2015) %>% full_join(mydata_1, by = "Patient.ID")


    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(stage_binary, year_2015) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    ## `summarise()` has grouped output by 'stage_binary'. You can override using the `.groups` argument.

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">stage_binary</th>
<th style="text-align: left;">year_2015</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Early stage</td>
<td style="text-align: left;">After 2015</td>
<td style="text-align: right;">64140</td>
<td style="text-align: right;">9.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Early stage</td>
<td style="text-align: left;">Before 2015</td>
<td style="text-align: right;">152625</td>
<td style="text-align: right;">21.7</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Late stage</td>
<td style="text-align: left;">After 2015</td>
<td style="text-align: right;">132568</td>
<td style="text-align: right;">18.9</td>
</tr>
<tr class="even">
<td style="text-align: left;">Late stage</td>
<td style="text-align: left;">Before 2015</td>
<td style="text-align: right;">296172</td>
<td style="text-align: right;">42.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NA</td>
<td style="text-align: left;">NA</td>
<td style="text-align: right;">57498</td>
<td style="text-align: right;">8.2</td>
</tr>
</tbody>
</table>

#### Tumor sequence number

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(Sequence.number) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">Sequence.number</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">1st of 2 or more primaries</td>
<td style="text-align: right;">55034</td>
<td style="text-align: right;">7.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">One primary only</td>
<td style="text-align: right;">647969</td>
<td style="text-align: right;">92.2</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(Sequence.number) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = Sequence.number)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.4, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Sequence.number", y = "Counts (*1000)", x = "") +
      scale_y_continuous(limits = c(0, 700)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-66-1.png)

### Treatment

#### Days from diagnosis to treatment

    mydata_1 <- mydata_1 %>%
      mutate(time_from_diagnosis_to_treatment = ifelse(Time.from.diagnosis.to.treatment.in.days.recode == "731+ days", 731, Time.from.diagnosis.to.treatment.in.days.recode)) %>% 
      mutate(time_from_diagnosis_to_treatment_1 = ifelse(time_from_diagnosis_to_treatment == "Unable to calculate", NA_character_, time_from_diagnosis_to_treatment)) %>% 
      mutate(time_from_diagnosis_to_treatment_2 = as.numeric(time_from_diagnosis_to_treatment_1)) %>% 
      mutate(radiation = case_when(
        Radiation.recode %in% c("Beam radiation", "Combination of beam with implants or isotopes", "Radiation, NOS  method or source not specified", "Radioactive implants (includes brachytherapy) (1988+)", "Radioisotopes (1988+)") ~ "Yes",
        Radiation.recode %in% c("None/Unknown", "Recommended, unknown if administered", "Refused (1988+)") ~ "None/Refused/Unknown"
      )) %>% 
      mutate(surgery = case_when(
        Reason.no.cancer.directed.surgery == "Surgery performed" ~ "Yes",
        Reason.no.cancer.directed.surgery %in% c("Not performed, patient died prior to recommended surgery", "Not recommended, contraindicated due to other cond; autopsy only (1973-2002)", "Recommended but not performed, unknown reason", "Not recommended", "Recommended but not performed, patient refused", "Recommended, unknown if performed", "Unknown; death certificate; or autopsy only (2003+)") ~ "None/Refused/Unknown"
      ))

    summary(mydata_1$time_from_diagnosis_to_treatment_2)  # Gives Min, 1st Qu., Median, Mean, 3rd Qu., Max

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
    ##    0.00    7.00   25.00   34.31   47.00  731.00  204242

    # Create a histogram of the age column
    ggplot(mydata_1, aes(x = time_from_diagnosis_to_treatment_2)) +
      geom_histogram(binwidth = 10, fill = "lightblue", color = "black") +
      scale_x_continuous(breaks = seq(0, 750, by = 30)) +
      xlab("Days") +
      ylab("Cases") +
      ggtitle("Days from diagnosis to treatment")

    ## Warning: Removed 204242 rows containing non-finite outside the scale range (`stat_bin()`).

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-67-1.png)

#### Chemotherapy (Binary)

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(Chemotherapy.recode..yes..no.unk.) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">Chemotherapy.recode..yes..no.unk.</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">No/Unknown</td>
<td style="text-align: right;">384179</td>
<td style="text-align: right;">54.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">Yes</td>
<td style="text-align: right;">318824</td>
<td style="text-align: right;">45.4</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(Chemotherapy.recode..yes..no.unk.) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = Chemotherapy.recode..yes..no.unk.)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.3, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Chemotherapy", y = "Counts (*1000)", x = "") +
      scale_y_continuous(limits = c(0, 400)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-68-1.png)

#### Radiation (Binary)

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(radiation) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">radiation</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">None/Refused/Unknown</td>
<td style="text-align: right;">421944</td>
<td style="text-align: right;">60</td>
</tr>
<tr class="even">
<td style="text-align: left;">Yes</td>
<td style="text-align: right;">281059</td>
<td style="text-align: right;">40</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(radiation) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = radiation)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.3, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Radiation", y = "Counts (*1000)", x = "") +
      scale_y_continuous(limits = c(0, 450)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-69-1.png)

#### Surgery (Binary)

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(surgery) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">surgery</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">None/Refused/Unknown</td>
<td style="text-align: right;">540047</td>
<td style="text-align: right;">76.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">Yes</td>
<td style="text-align: right;">162956</td>
<td style="text-align: right;">23.2</td>
</tr>
</tbody>
</table>

    # Calculate percentage frequencies
    mydata_1 <- mydata_1 %>%
      group_by(surgery) %>%
      mutate(Count = n()) %>% 
      mutate(Percentage = Count / nrow(mydata_1) * 100) %>% ungroup()

    # Create barplot
    ggplot(mydata_1, aes(x = surgery)) +
      geom_bar(aes(y = after_stat(count) / 1000), width = 0.3, fill = "lightblue", color = "darkblue") +
      geom_text(aes(y = after_stat(count) / 1000, label = sprintf("%.1f%%", Percentage)), 
                stat = "count", vjust = -0.5, color = "black") +  # Add percentages on top of bars
      labs(title = "Surgery", y = "Counts (*1000)", x = "") +
      scale_y_continuous(limits = c(0, 600)) +
      theme_minimal() +  # Optional: Use a minimal theme
      theme(plot.title = element_text(hjust = 0.5))  # Center the title

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-70-1.png)

### Vital status (Binary)

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(Vital.status.recode..study.cutoff.used.) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th
style="text-align: left;">Vital.status.recode..study.cutoff.used.</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Alive</td>
<td style="text-align: right;">115803</td>
<td style="text-align: right;">16.5</td>
</tr>
<tr class="even">
<td style="text-align: left;">Dead</td>
<td style="text-align: right;">587200</td>
<td style="text-align: right;">83.5</td>
</tr>
</tbody>
</table>

### Cause of death

#### Cause of death 1

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(SEER.other.cause.of.death.classification) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<colgroup>
<col style="width: 75%" />
<col style="width: 9%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th
style="text-align: left;">SEER.other.cause.of.death.classification</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Alive or dead due to cancer</td>
<td style="text-align: right;">615314</td>
<td style="text-align: right;">87.5</td>
</tr>
<tr class="even">
<td style="text-align: left;">Dead (attributable to causes other than
this cancer dx)</td>
<td style="text-align: right;">81854</td>
<td style="text-align: right;">11.6</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Dead (missing/unknown COD)</td>
<td style="text-align: right;">5835</td>
<td style="text-align: right;">0.8</td>
</tr>
</tbody>
</table>

#### Cause of death 2

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(SEER.cause.specific.death.classification) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup()

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th
style="text-align: left;">SEER.cause.specific.death.classification</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Alive or dead of other cause</td>
<td style="text-align: right;">197657</td>
<td style="text-align: right;">28.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Dead (attributable to this cancer dx)</td>
<td style="text-align: right;">499511</td>
<td style="text-align: right;">71.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Dead (missing/unknown COD)</td>
<td style="text-align: right;">5835</td>
<td style="text-align: right;">0.8</td>
</tr>
</tbody>
</table>

#### Cause of death 3

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(COD.to.site.recode.ICD.O.3.2023.Revision.Expanded..1999..) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup() %>% arrange(desc(Count))

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<colgroup>
<col style="width: 81%" />
<col style="width: 7%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th
style="text-align: left;">COD.to.site.recode.ICD.O.3.2023.Revision.Expanded..1999..</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Lung And Bronchus</td>
<td style="text-align: right;">473467</td>
<td style="text-align: right;">67.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">Alive</td>
<td style="text-align: right;">115803</td>
<td style="text-align: right;">16.5</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Miscellaneous Neoplasms</td>
<td style="text-align: right;">16893</td>
<td style="text-align: right;">2.4</td>
</tr>
<tr class="even">
<td style="text-align: left;">Chronic Obstructive Pulmonary Disease and
Allied Conditions</td>
<td style="text-align: right;">15838</td>
<td style="text-align: right;">2.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Ischemic heart disease</td>
<td style="text-align: right;">14416</td>
<td style="text-align: right;">2.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Other COD</td>
<td style="text-align: right;">12495</td>
<td style="text-align: right;">1.8</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Other and unspecified disorders of the
circulatory system</td>
<td style="text-align: right;">6801</td>
<td style="text-align: right;">1.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">State DC not available or state DC
available but no COD</td>
<td style="text-align: right;">5835</td>
<td style="text-align: right;">0.8</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Cerebrovascular diseases</td>
<td style="text-align: right;">4318</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">Pneumonia and Influenza</td>
<td style="text-align: right;">2751</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Accidents and Adverse Effects</td>
<td style="text-align: right;">2344</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">Septicemia</td>
<td style="text-align: right;">2101</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Hypertensive disease</td>
<td style="text-align: right;">1866</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">COVID (2020+ only)</td>
<td style="text-align: right;">1602</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Diabetes Mellitus</td>
<td style="text-align: right;">1590</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">Symptoms, Signs and Ill-Defined
Conditions</td>
<td style="text-align: right;">1531</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Other infectious and Parasitic Diseases
incl HIV</td>
<td style="text-align: right;">1466</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">Alzheimers (ICD-9 and ICD-10 only)</td>
<td style="text-align: right;">1346</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Pancreas</td>
<td style="text-align: right;">1317</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">Colon And Rectum (Excluding Appendix)</td>
<td style="text-align: right;">1278</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Nephritis, Nephrotic Syndrome and
Nephrosis</td>
<td style="text-align: right;">1265</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">Breast</td>
<td style="text-align: right;">1186</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Diseases of arteries, arterioles and
capillaries</td>
<td style="text-align: right;">1101</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">Liver</td>
<td style="text-align: right;">1058</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Brain (Malignant)</td>
<td style="text-align: right;">1006</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Benign and Borderline: All Other
sites</td>
<td style="text-align: right;">889</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Suicide and Self-Inflicted Injury</td>
<td style="text-align: right;">795</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Esophagus</td>
<td style="text-align: right;">712</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Pulmonary heart disease and diseases of
pulmonary circulation</td>
<td style="text-align: right;">695</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Miscellaneous Hematopoietic Neoplasms</td>
<td style="text-align: right;">675</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Chronic Liver Disease and Cirrhosis</td>
<td style="text-align: right;">586</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Prostate</td>
<td style="text-align: right;">527</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Kidney Parenchyma</td>
<td style="text-align: right;">474</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Urinary Bladder</td>
<td style="text-align: right;">471</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Other B-cell leukemia/lymphomas or
Lymphoma, NOS</td>
<td style="text-align: right;">460</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Soft Tissue</td>
<td style="text-align: right;">421</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Stomach</td>
<td style="text-align: right;">357</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">Acute Myeloid Leukemias</td>
<td style="text-align: right;">345</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Brain, CNS Other and Intracranial Gland
(Benign and Borderline)</td>
<td style="text-align: right;">302</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Mesothelioma</td>
<td style="text-align: right;">256</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Other Non-Epithelial Skin</td>
<td style="text-align: right;">250</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Ovary</td>
<td style="text-align: right;">236</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Stomach and Duodenal Ulcers</td>
<td style="text-align: right;">230</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Complications of medical and surgical care
(Y40-Y84, Y88) (ICD-10 only, 1999+)</td>
<td style="text-align: right;">226</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Heart, Mediastinum And Pleura</td>
<td style="text-align: right;">219</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Larynx</td>
<td style="text-align: right;">215</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Plasma Cell Neoplasms</td>
<td style="text-align: right;">198</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Other Leukemias</td>
<td style="text-align: right;">180</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Myelodysplastic Syndromes</td>
<td style="text-align: right;">177</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Melanoma Of The Skin</td>
<td style="text-align: right;">174</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Bones And Joints</td>
<td style="text-align: right;">173</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Trachea, And Respiratory Other</td>
<td style="text-align: right;">137</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Intrahepatic Bile Duct</td>
<td style="text-align: right;">134</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Adrenal Gland</td>
<td style="text-align: right;">121</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Pharynx And Oral Cavity Other</td>
<td style="text-align: right;">121</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Corpus</td>
<td style="text-align: right;">113</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Digestive Other</td>
<td style="text-align: right;">97</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Thyroid</td>
<td style="text-align: right;">90</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Chronic lymphocytic leukemia (CLL)/Small
lymphocytic lymphoma</td>
<td style="text-align: right;">86</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Congenital Anomalies</td>
<td style="text-align: right;">73</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Small Intestine</td>
<td style="text-align: right;">73</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Oropharynx</td>
<td style="text-align: right;">68</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Tongue Anterior</td>
<td style="text-align: right;">66</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Myeloproliferative/Myelodysplastic
syndromes, including MDS/MPN overlap</td>
<td style="text-align: right;">59</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Homicide and Legal Intervention</td>
<td style="text-align: right;">52</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Large B-cell lymphoma</td>
<td style="text-align: right;">52</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Complications of Pregnancy, Childbrith,
Puerperium</td>
<td style="text-align: right;">45</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Cervix</td>
<td style="text-align: right;">44</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Mouth Other</td>
<td style="text-align: right;">41</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Gallbladder</td>
<td style="text-align: right;">40</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">In situ neoplasms</td>
<td style="text-align: right;">39</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Thymus</td>
<td style="text-align: right;">38</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Meninges (Malignant)</td>
<td style="text-align: right;">37</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Endocrine Other</td>
<td style="text-align: right;">34</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Retroperitoneum And Peritoneum</td>
<td style="text-align: right;">32</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Biliary Other</td>
<td style="text-align: right;">31</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Nasopharynx</td>
<td style="text-align: right;">30</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Major Salivary Glands</td>
<td style="text-align: right;">29</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Precursor Lymphoid Neoplasms</td>
<td style="text-align: right;">28</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">CNS Other (Malignant)</td>
<td style="text-align: right;">26</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Anus, Anal Canal And Anorectum</td>
<td style="text-align: right;">22</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Hodgkin Lymphomas</td>
<td style="text-align: right;">21</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Other T and NK-cell
leukemias/lymphomas</td>
<td style="text-align: right;">21</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Extrahepatic Bile Ducts</td>
<td style="text-align: right;">15</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Testis</td>
<td style="text-align: right;">14</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Ureter</td>
<td style="text-align: right;">13</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Hypopharynx</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Kidney Renal Pelvis</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Sinus Other</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Urinary Other</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Vulva</td>
<td style="text-align: right;">10</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Appendix</td>
<td style="text-align: right;">9</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Kaposi Sarcoma</td>
<td style="text-align: right;">8</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Ampulla Of Vater</td>
<td style="text-align: right;">7</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Certain Conditions Originating in
Perinatal Period</td>
<td style="text-align: right;">7</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Nasal Cavity And Paranasal Sinuses</td>
<td style="text-align: right;">7</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Urethra</td>
<td style="text-align: right;">6</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Fallopian Tube</td>
<td style="text-align: right;">5</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Gum</td>
<td style="text-align: right;">5</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Lip</td>
<td style="text-align: right;">5</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Penis</td>
<td style="text-align: right;">5</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Vagina</td>
<td style="text-align: right;">5</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Adnexa Other And Genital Female Other</td>
<td style="text-align: right;">4</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Intracranial Gland (Malignant)</td>
<td style="text-align: right;">4</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Eye And Orbit</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Floor Of Mouth</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Placenta</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Buccal Mucosa</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Genital Male Other</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Mycosis Fungoides/Sezary Syndrome</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Parathyroid</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">0.0</td>
</tr>
</tbody>
</table>

### County

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(State.county) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup() %>% arrange(desc(Count))

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">State.county</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">CA: Los Angeles Registry (06037)</td>
<td style="text-align: right;">56844</td>
<td style="text-align: right;">8.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: San Diego County (06073)</td>
<td style="text-align: right;">21741</td>
<td style="text-align: right;">3.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Orange County (06059)</td>
<td style="text-align: right;">19615</td>
<td style="text-align: right;">2.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Riverside County (06065)</td>
<td style="text-align: right;">14690</td>
<td style="text-align: right;">2.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">WA: King County (53033)</td>
<td style="text-align: right;">13752</td>
<td style="text-align: right;">2.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: San Bernardino County (06071)</td>
<td style="text-align: right;">11665</td>
<td style="text-align: right;">1.7</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Sacramento County (06067)</td>
<td style="text-align: right;">11527</td>
<td style="text-align: right;">1.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Jefferson County (21111)</td>
<td style="text-align: right;">11075</td>
<td style="text-align: right;">1.6</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Santa Clara County (06085)</td>
<td style="text-align: right;">10518</td>
<td style="text-align: right;">1.5</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Alameda County (06001)</td>
<td style="text-align: right;">10333</td>
<td style="text-align: right;">1.5</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CT: New Haven County (09009)</td>
<td style="text-align: right;">10116</td>
<td style="text-align: right;">1.4</td>
</tr>
<tr class="even">
<td style="text-align: left;">CT: Hartford County (09003)</td>
<td style="text-align: right;">9969</td>
<td style="text-align: right;">1.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Ocean County (34029)</td>
<td style="text-align: right;">9476</td>
<td style="text-align: right;">1.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Bergen County (34003)</td>
<td style="text-align: right;">8522</td>
<td style="text-align: right;">1.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">HI: Honolulu County (15003) - 2000+</td>
<td style="text-align: right;">8380</td>
<td style="text-align: right;">1.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">CT: Fairfield County (09001)</td>
<td style="text-align: right;">8356</td>
<td style="text-align: right;">1.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">WA: Pierce County (53053)</td>
<td style="text-align: right;">8010</td>
<td style="text-align: right;">1.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Contra Costa County (06013)</td>
<td style="text-align: right;">7762</td>
<td style="text-align: right;">1.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Middlesex County (34023)</td>
<td style="text-align: right;">6983</td>
<td style="text-align: right;">1.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: San Francisco County (06075)</td>
<td style="text-align: right;">6893</td>
<td style="text-align: right;">1.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Monmouth County (34025)</td>
<td style="text-align: right;">6852</td>
<td style="text-align: right;">1.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Fulton County (13121)</td>
<td style="text-align: right;">6601</td>
<td style="text-align: right;">0.9</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Essex County (34013)</td>
<td style="text-align: right;">6236</td>
<td style="text-align: right;">0.9</td>
</tr>
<tr class="even">
<td style="text-align: left;">WA: Snohomish County (53061)</td>
<td style="text-align: right;">6178</td>
<td style="text-align: right;">0.9</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Camden County (34007)</td>
<td style="text-align: right;">5826</td>
<td style="text-align: right;">0.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Fresno County (06019)</td>
<td style="text-align: right;">5796</td>
<td style="text-align: right;">0.8</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Kern County (06029)</td>
<td style="text-align: right;">5319</td>
<td style="text-align: right;">0.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Jefferson Parish (22051)</td>
<td style="text-align: right;">5273</td>
<td style="text-align: right;">0.8</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Ventura County (06111)</td>
<td style="text-align: right;">5243</td>
<td style="text-align: right;">0.7</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: San Mateo County (06081)</td>
<td style="text-align: right;">5130</td>
<td style="text-align: right;">0.7</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: San Joaquin County (06077)</td>
<td style="text-align: right;">5119</td>
<td style="text-align: right;">0.7</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Burlington County (34005)</td>
<td style="text-align: right;">4814</td>
<td style="text-align: right;">0.7</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Cobb County (13067)</td>
<td style="text-align: right;">4812</td>
<td style="text-align: right;">0.7</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: DeKalb County (13089)</td>
<td style="text-align: right;">4677</td>
<td style="text-align: right;">0.7</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Polk County (19153)</td>
<td style="text-align: right;">4555</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Gwinnett County (13135)</td>
<td style="text-align: right;">4451</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Hudson County (34017)</td>
<td style="text-align: right;">4332</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Union County (34039)</td>
<td style="text-align: right;">4206</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Morris County (34027)</td>
<td style="text-align: right;">4190</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Bernalillo County (35001)</td>
<td style="text-align: right;">4110</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Passaic County (34031)</td>
<td style="text-align: right;">4081</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Orleans Parish (22071)</td>
<td style="text-align: right;">4064</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Sonoma County (06097)</td>
<td style="text-align: right;">3899</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Stanislaus County (06099)</td>
<td style="text-align: right;">3886</td>
<td style="text-align: right;">0.6</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Salt Lake County (49035)</td>
<td style="text-align: right;">3717</td>
<td style="text-align: right;">0.5</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Solano County (06095)</td>
<td style="text-align: right;">3626</td>
<td style="text-align: right;">0.5</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: East Baton Rouge Parish (22033)</td>
<td style="text-align: right;">3611</td>
<td style="text-align: right;">0.5</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Mercer County (34021)</td>
<td style="text-align: right;">3450</td>
<td style="text-align: right;">0.5</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CT: New London County (09011)</td>
<td style="text-align: right;">3384</td>
<td style="text-align: right;">0.5</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Gloucester County (34015)</td>
<td style="text-align: right;">3367</td>
<td style="text-align: right;">0.5</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Atlantic County (34001)</td>
<td style="text-align: right;">3294</td>
<td style="text-align: right;">0.5</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Caddo Parish (22017)</td>
<td style="text-align: right;">3198</td>
<td style="text-align: right;">0.5</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Fayette County (21067)</td>
<td style="text-align: right;">3096</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Placer County (06061)</td>
<td style="text-align: right;">2838</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Chatham County (13051)</td>
<td style="text-align: right;">2826</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Santa Barbara County (06083)</td>
<td style="text-align: right;">2780</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: St. Tammany Parish (22103)</td>
<td style="text-align: right;">2531</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="even">
<td style="text-align: left;">WA: Kitsap County (53035)</td>
<td style="text-align: right;">2507</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Butte County (06007)</td>
<td style="text-align: right;">2497</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="even">
<td style="text-align: left;">WA: Thurston County (53067)</td>
<td style="text-align: right;">2481</td>
<td style="text-align: right;">0.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Monterey County (06053)</td>
<td style="text-align: right;">2447</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Tulare County (06107)</td>
<td style="text-align: right;">2426</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CT: Litchfield County (09005)</td>
<td style="text-align: right;">2411</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Richmond County (13245)</td>
<td style="text-align: right;">2397</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: San Luis Obispo County (06079)</td>
<td style="text-align: right;">2372</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Calcasieu Parish (22019)</td>
<td style="text-align: right;">2365</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Somerset County (34035)</td>
<td style="text-align: right;">2360</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Linn County (19113)</td>
<td style="text-align: right;">2319</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Shasta County (06089)</td>
<td style="text-align: right;">2290</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Kenton County (21117)</td>
<td style="text-align: right;">2288</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Lafayette Parish (22055)</td>
<td style="text-align: right;">2202</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Muscogee County (13215)</td>
<td style="text-align: right;">2091</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CT: Middlesex County (09007)</td>
<td style="text-align: right;">1962</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Bibb County (13021)</td>
<td style="text-align: right;">1946</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Scott County (19163)</td>
<td style="text-align: right;">1887</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Ouachita Parish (22073)</td>
<td style="text-align: right;">1885</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Cherokee County (13057)</td>
<td style="text-align: right;">1875</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Clayton County (13063)</td>
<td style="text-align: right;">1841</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Marin County (06041)</td>
<td style="text-align: right;">1815</td>
<td style="text-align: right;">0.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Hall County (13139)</td>
<td style="text-align: right;">1755</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Rapides Parish (22079)</td>
<td style="text-align: right;">1750</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Cumberland County (34011)</td>
<td style="text-align: right;">1731</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Cape May County (34009)</td>
<td style="text-align: right;">1700</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">HI: Hawaii County (15001) - 2000+</td>
<td style="text-align: right;">1680</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">WA: Whatcom County (53073)</td>
<td style="text-align: right;">1674</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Daviess County (21059)</td>
<td style="text-align: right;">1663</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Black Hawk County (19013)</td>
<td style="text-align: right;">1617</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Santa Cruz County (06087)</td>
<td style="text-align: right;">1559</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: El Dorado County (06017)</td>
<td style="text-align: right;">1554</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Henry County (13151)</td>
<td style="text-align: right;">1548</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ: Sussex County (34037)</td>
<td style="text-align: right;">1541</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Hardin County (21093)</td>
<td style="text-align: right;">1535</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Merced County (06047)</td>
<td style="text-align: right;">1512</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">CT: Windham County (09015)</td>
<td style="text-align: right;">1466</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CT: Tolland County (09013)</td>
<td style="text-align: right;">1465</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Terrebonne Parish (22109)</td>
<td style="text-align: right;">1453</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Warren County (21227)</td>
<td style="text-align: right;">1446</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Houston County (13153)</td>
<td style="text-align: right;">1441</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Campbell County (21037)</td>
<td style="text-align: right;">1402</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Pike County (21195)</td>
<td style="text-align: right;">1383</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Livingston Parish (22063)</td>
<td style="text-align: right;">1379</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Humboldt County (06023)</td>
<td style="text-align: right;">1369</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Floyd County (13115)</td>
<td style="text-align: right;">1364</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Pottawattamie County (19155)</td>
<td style="text-align: right;">1337</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Boone County (21015)</td>
<td style="text-align: right;">1304</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Tangipahoa Parish (22105)</td>
<td style="text-align: right;">1296</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Bartow County (13015)</td>
<td style="text-align: right;">1288</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Dona Ana County (35013)</td>
<td style="text-align: right;">1265</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Bossier Parish (22015)</td>
<td style="text-align: right;">1262</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Warren County (34041)</td>
<td style="text-align: right;">1258</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Forsyth County (13117)</td>
<td style="text-align: right;">1256</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">WA: Skagit County (53057)</td>
<td style="text-align: right;">1256</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Carroll County (13045)</td>
<td style="text-align: right;">1252</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Paulding County (13223)</td>
<td style="text-align: right;">1240</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Whitfield County (13313)</td>
<td style="text-align: right;">1224</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Woodbury County (19193)</td>
<td style="text-align: right;">1222</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">HI: Maui County (15009) - 2000+</td>
<td style="text-align: right;">1220</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Yolo County (06113)</td>
<td style="text-align: right;">1217</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: St. Landry Parish (22097)</td>
<td style="text-align: right;">1192</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Coweta County (13077)</td>
<td style="text-align: right;">1190</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Douglas County (13097)</td>
<td style="text-align: right;">1171</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Napa County (06055)</td>
<td style="text-align: right;">1153</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">WA: Grays Harbor County (53027)</td>
<td style="text-align: right;">1133</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Walker County (13295)</td>
<td style="text-align: right;">1129</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Pulaski County (21199)</td>
<td style="text-align: right;">1123</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Bullitt County (21029)</td>
<td style="text-align: right;">1122</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">WA: Clallam County (53009)</td>
<td style="text-align: right;">1114</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: McCracken County (21145)</td>
<td style="text-align: right;">1103</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Dougherty County (13095)</td>
<td style="text-align: right;">1098</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Lafourche Parish (22057)</td>
<td style="text-align: right;">1088</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Madera County (06039)</td>
<td style="text-align: right;">1073</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Columbia County (13073)</td>
<td style="text-align: right;">1066</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Nevada County (06057)</td>
<td style="text-align: right;">1055</td>
<td style="text-align: right;">0.2</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Hunterdon County (34019)</td>
<td style="text-align: right;">1052</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Glynn County (13127)</td>
<td style="text-align: right;">1050</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Madison County (21151)</td>
<td style="text-align: right;">1050</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Lake County (06033)</td>
<td style="text-align: right;">1027</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Laurel County (21125)</td>
<td style="text-align: right;">1018</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Floyd County (21071)</td>
<td style="text-align: right;">995</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Dubuque County (19061)</td>
<td style="text-align: right;">983</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Weber County (49057)</td>
<td style="text-align: right;">983</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Lowndes County (13185)</td>
<td style="text-align: right;">982</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Newton County (13217)</td>
<td style="text-align: right;">982</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Ascension Parish (22005)</td>
<td style="text-align: right;">976</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Imperial County (06025)</td>
<td style="text-align: right;">973</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">WA: Mason County (53045)</td>
<td style="text-align: right;">969</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Boyd County (21019)</td>
<td style="text-align: right;">929</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Salem County (34033)</td>
<td style="text-align: right;">902</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Iberia Parish (22045)</td>
<td style="text-align: right;">894</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Mendocino County (06045)</td>
<td style="text-align: right;">893</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Walton County (13297)</td>
<td style="text-align: right;">890</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Spalding County (13255)</td>
<td style="text-align: right;">874</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Sutter County (06101)</td>
<td style="text-align: right;">866</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Hopkins County (21107)</td>
<td style="text-align: right;">861</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Santa Fe County (35049)</td>
<td style="text-align: right;">844</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Fayette County (13113)</td>
<td style="text-align: right;">843</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Utah County (49049)</td>
<td style="text-align: right;">832</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Tehama County (06103)</td>
<td style="text-align: right;">830</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Christian County (21047)</td>
<td style="text-align: right;">827</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Acadia Parish (22001)</td>
<td style="text-align: right;">822</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">WA: Island County (53029)</td>
<td style="text-align: right;">822</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Troup County (13285)</td>
<td style="text-align: right;">817</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Washington County (49053)</td>
<td style="text-align: right;">810</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Yuba County (06115)</td>
<td style="text-align: right;">794</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Barren County (21009)</td>
<td style="text-align: right;">794</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Sandoval County (35043)</td>
<td style="text-align: right;">792</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Kings County (06031)</td>
<td style="text-align: right;">789</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Catoosa County (13047)</td>
<td style="text-align: right;">784</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Davis County (49011)</td>
<td style="text-align: right;">782</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Franklin County (21073)</td>
<td style="text-align: right;">779</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: San Juan County (35045)</td>
<td style="text-align: right;">778</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Henderson County (21101)</td>
<td style="text-align: right;">777</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Johnson County (19103)</td>
<td style="text-align: right;">775</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Perry County (21193)</td>
<td style="text-align: right;">773</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Whitley County (21235)</td>
<td style="text-align: right;">768</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Gordon County (13129)</td>
<td style="text-align: right;">766</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Clarke County (13059)</td>
<td style="text-align: right;">746</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Greenup County (21089)</td>
<td style="text-align: right;">741</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Rockdale County (13247)</td>
<td style="text-align: right;">739</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Jackson County (13157)</td>
<td style="text-align: right;">738</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Barrow County (13013)</td>
<td style="text-align: right;">723</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Tuolumne County (06109)</td>
<td style="text-align: right;">717</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Knox County (21121)</td>
<td style="text-align: right;">713</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Vermilion Parish (22113)</td>
<td style="text-align: right;">711</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Washington Parish (22117)</td>
<td style="text-align: right;">711</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Polk County (13233)</td>
<td style="text-align: right;">688</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: St. Mary Parish (22101)</td>
<td style="text-align: right;">681</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Thomas County (13275)</td>
<td style="text-align: right;">669</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Webster Parish (22119)</td>
<td style="text-align: right;">668</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Clinton County (19045)</td>
<td style="text-align: right;">665</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Harlan County (21095)</td>
<td style="text-align: right;">665</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: St. Bernard Parish (22087)</td>
<td style="text-align: right;">662</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Oldham County (21185)</td>
<td style="text-align: right;">656</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Des Moines County (19057)</td>
<td style="text-align: right;">653</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Avoyelles Parish (22009)</td>
<td style="text-align: right;">653</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: St. Martin Parish (22099)</td>
<td style="text-align: right;">645</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Laurens County (13175)</td>
<td style="text-align: right;">642</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Bulloch County (13031)</td>
<td style="text-align: right;">641</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Jessamine County (21113)</td>
<td style="text-align: right;">640</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Otero County (35035)</td>
<td style="text-align: right;">637</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Cerro Gordo County (19033)</td>
<td style="text-align: right;">629</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Graves County (21083)</td>
<td style="text-align: right;">628</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Muhlenberg County (21177)</td>
<td style="text-align: right;">628</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Nelson County (21179)</td>
<td style="text-align: right;">624</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Effingham County (13103)</td>
<td style="text-align: right;">623</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Murray County (13213)</td>
<td style="text-align: right;">612</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Colquitt County (13071)</td>
<td style="text-align: right;">609</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Marshall County (21157)</td>
<td style="text-align: right;">604</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Chaves County (35005)</td>
<td style="text-align: right;">597</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Story County (19169)</td>
<td style="text-align: right;">595</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Vernon Parish (22115)</td>
<td style="text-align: right;">588</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">HI: Kauai County (15007) - 2000+</td>
<td style="text-align: right;">587</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Valencia County (35061) - 1982+</td>
<td style="text-align: right;">584</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Shelby County (21211)</td>
<td style="text-align: right;">566</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Siskiyou County (06093)</td>
<td style="text-align: right;">565</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Clark County (21049)</td>
<td style="text-align: right;">565</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Baldwin County (13009)</td>
<td style="text-align: right;">559</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Bell County (21013)</td>
<td style="text-align: right;">552</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Logan County (21141)</td>
<td style="text-align: right;">550</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Carter County (21043)</td>
<td style="text-align: right;">547</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Wapello County (19179)</td>
<td style="text-align: right;">545</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Webster County (19187)</td>
<td style="text-align: right;">531</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Dallas County (19049)</td>
<td style="text-align: right;">529</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Calaveras County (06009)</td>
<td style="text-align: right;">528</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Grayson County (21085)</td>
<td style="text-align: right;">525</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Calloway County (21035)</td>
<td style="text-align: right;">521</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Habersham County (13137)</td>
<td style="text-align: right;">520</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Jasper County (19099)</td>
<td style="text-align: right;">514</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Lea County (35025)</td>
<td style="text-align: right;">510</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Lincoln County (21137)</td>
<td style="text-align: right;">509</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Amador County (06005)</td>
<td style="text-align: right;">505</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Letcher County (21133)</td>
<td style="text-align: right;">497</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Lee County (19111)</td>
<td style="text-align: right;">496</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Marshall County (19127)</td>
<td style="text-align: right;">496</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Eddy County (35015)</td>
<td style="text-align: right;">496</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Ware County (13299)</td>
<td style="text-align: right;">495</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: St. Charles Parish (22089)</td>
<td style="text-align: right;">491</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Warren County (19181)</td>
<td style="text-align: right;">485</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Evangeline Parish (22039)</td>
<td style="text-align: right;">485</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Liberty County (13179)</td>
<td style="text-align: right;">481</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Montgomery County (21173)</td>
<td style="text-align: right;">472</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Muscatine County (19139)</td>
<td style="text-align: right;">471</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Meade County (21163)</td>
<td style="text-align: right;">471</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Pickens County (13227)</td>
<td style="text-align: right;">470</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Beauregard Parish (22011)</td>
<td style="text-align: right;">470</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Scott County (21209)</td>
<td style="text-align: right;">462</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Iberville Parish (22047)</td>
<td style="text-align: right;">461</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">WA: Jefferson County (53031)</td>
<td style="text-align: right;">461</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Tift County (13277)</td>
<td style="text-align: right;">460</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Taylor County (21217)</td>
<td style="text-align: right;">459</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Camden County (13039)</td>
<td style="text-align: right;">458</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Natchitoches Parish (22069)</td>
<td style="text-align: right;">454</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Johnson County (21115)</td>
<td style="text-align: right;">453</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Coffee County (13069)</td>
<td style="text-align: right;">446</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Haralson County (13143)</td>
<td style="text-align: right;">445</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Chattooga County (13055)</td>
<td style="text-align: right;">442</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Madison County (13195)</td>
<td style="text-align: right;">440</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Ohio County (21183)</td>
<td style="text-align: right;">435</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Boyle County (21021)</td>
<td style="text-align: right;">432</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Wayne County (13305)</td>
<td style="text-align: right;">427</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: White County (13311)</td>
<td style="text-align: right;">426</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Jefferson Davis Parish (22053)</td>
<td style="text-align: right;">426</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Mercer County (21167)</td>
<td style="text-align: right;">424</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Gilmer County (13123)</td>
<td style="text-align: right;">417</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Clay County (21051)</td>
<td style="text-align: right;">415</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: McCreary County (21147)</td>
<td style="text-align: right;">410</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Morehouse Parish (22067)</td>
<td style="text-align: right;">409</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Lincoln Parish (22061)</td>
<td style="text-align: right;">407</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: St. John the Baptist Parish
(22095)</td>
<td style="text-align: right;">407</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Lumpkin County (13187)</td>
<td style="text-align: right;">402</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Fannin County (13111)</td>
<td style="text-align: right;">395</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Grant County (21081)</td>
<td style="text-align: right;">383</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: De Soto Parish (22031)</td>
<td style="text-align: right;">382</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Breckinridge County (21027)</td>
<td style="text-align: right;">376</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Upson County (13293)</td>
<td style="text-align: right;">374</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Russell County (21207)</td>
<td style="text-align: right;">372</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Wayne County (21231)</td>
<td style="text-align: right;">369</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Stephens County (13257)</td>
<td style="text-align: right;">368</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Hart County (21099)</td>
<td style="text-align: right;">368</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Sabine Parish (22085)</td>
<td style="text-align: right;">368</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Union County (13291)</td>
<td style="text-align: right;">366</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Marion County (19125)</td>
<td style="text-align: right;">366</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Sumter County (13261)</td>
<td style="text-align: right;">363</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Union Parish (22111)</td>
<td style="text-align: right;">363</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Hart County (13147)</td>
<td style="text-align: right;">361</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Jones County (13169)</td>
<td style="text-align: right;">360</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Bourbon County (21017)</td>
<td style="text-align: right;">357</td>
<td style="text-align: right;">0.1</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Toombs County (13279)</td>
<td style="text-align: right;">349</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Decatur County (13087)</td>
<td style="text-align: right;">347</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Woodford County (21239)</td>
<td style="text-align: right;">346</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Bryan County (13029)</td>
<td style="text-align: right;">345</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Knott County (21119)</td>
<td style="text-align: right;">345</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Mitchell County (13205)</td>
<td style="text-align: right;">344</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Harrison County (21097)</td>
<td style="text-align: right;">341</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Boone County (19015)</td>
<td style="text-align: right;">340</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Allen County (21003)</td>
<td style="text-align: right;">340</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Curry County (35009)</td>
<td style="text-align: right;">339</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Putnam County (13237)</td>
<td style="text-align: right;">336</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Breathitt County (21025)</td>
<td style="text-align: right;">331</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Monroe County (13207)</td>
<td style="text-align: right;">330</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Assumption Parish (22007)</td>
<td style="text-align: right;">328</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Franklin County (13119)</td>
<td style="text-align: right;">325</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Worth County (13321)</td>
<td style="text-align: right;">325</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Butts County (13035)</td>
<td style="text-align: right;">324</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Harris County (13145)</td>
<td style="text-align: right;">324</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Peach County (13225)</td>
<td style="text-align: right;">324</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Rockcastle County (21203)</td>
<td style="text-align: right;">323</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Richland Parish (22083)</td>
<td style="text-align: right;">322</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Elbert County (13105)</td>
<td style="text-align: right;">321</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Grant Parish (22043)</td>
<td style="text-align: right;">321</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Tattnall County (13267)</td>
<td style="text-align: right;">317</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Estill County (21065)</td>
<td style="text-align: right;">315</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Anderson County (21005)</td>
<td style="text-align: right;">314</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Benton County (19011)</td>
<td style="text-align: right;">309</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Rowan County (21205)</td>
<td style="text-align: right;">308</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Pierce County (13229)</td>
<td style="text-align: right;">306</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Simpson County (21213)</td>
<td style="text-align: right;">306</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Crisp County (13081)</td>
<td style="text-align: right;">305</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Lee County (13177)</td>
<td style="text-align: right;">305</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Garrard County (21079)</td>
<td style="text-align: right;">303</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Adair County (21001)</td>
<td style="text-align: right;">302</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Leslie County (21131)</td>
<td style="text-align: right;">300</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Marion County (21155)</td>
<td style="text-align: right;">300</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Powell County (21197)</td>
<td style="text-align: right;">300</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Dodge County (13091)</td>
<td style="text-align: right;">299</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Emanuel County (13107)</td>
<td style="text-align: right;">299</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Lawrence County (21127)</td>
<td style="text-align: right;">299</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Grady County (13131)</td>
<td style="text-align: right;">297</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Dawson County (13085)</td>
<td style="text-align: right;">295</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Del Norte County (06015)</td>
<td style="text-align: right;">293</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Mason County (21161)</td>
<td style="text-align: right;">293</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Allen Parish (22003)</td>
<td style="text-align: right;">292</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Burke County (13033)</td>
<td style="text-align: right;">291</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Casey County (21045)</td>
<td style="text-align: right;">291</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: McDuffie County (13189)</td>
<td style="text-align: right;">290</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Lewis County (21135)</td>
<td style="text-align: right;">290</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Meriwether County (13199)</td>
<td style="text-align: right;">289</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Trigg County (21221)</td>
<td style="text-align: right;">289</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: West Baton Rouge Parish (22121)</td>
<td style="text-align: right;">288</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Pendleton County (21191)</td>
<td style="text-align: right;">285</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Franklin Parish (22041)</td>
<td style="text-align: right;">281</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Plaquemines Parish (22075)</td>
<td style="text-align: right;">281</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Glenn County (06021)</td>
<td style="text-align: right;">278</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Mahaska County (19123)</td>
<td style="text-align: right;">276</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Edmonson County (21061)</td>
<td style="text-align: right;">276</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Plumas County (06063)</td>
<td style="text-align: right;">274</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Henry County (21103)</td>
<td style="text-align: right;">274</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Pointe Coupee Parish (22077)</td>
<td style="text-align: right;">274</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Brantley County (13025)</td>
<td style="text-align: right;">270</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Fayette County (19065)</td>
<td style="text-align: right;">270</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Concordia Parish (22029)</td>
<td style="text-align: right;">269</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Page County (19145)</td>
<td style="text-align: right;">268</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Jones County (19105)</td>
<td style="text-align: right;">267</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: East Feliciana Parish (22037)</td>
<td style="text-align: right;">264</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: San Benito County (06069)</td>
<td style="text-align: right;">263</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Buchanan County (19019)</td>
<td style="text-align: right;">261</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Grant County (35017)</td>
<td style="text-align: right;">261</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Washington County (13303)</td>
<td style="text-align: right;">260</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Henry County (19087)</td>
<td style="text-align: right;">260</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Ben Hill County (13017)</td>
<td style="text-align: right;">259</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Jackson County (21109)</td>
<td style="text-align: right;">258</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Jackson County (19097)</td>
<td style="text-align: right;">255</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Carroll County (19027)</td>
<td style="text-align: right;">254</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Jackson Parish (22049)</td>
<td style="text-align: right;">254</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Crawford County (13079)</td>
<td style="text-align: right;">253</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Berrien County (13019)</td>
<td style="text-align: right;">251</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Martin County (21159)</td>
<td style="text-align: right;">251</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Butler County (21031)</td>
<td style="text-align: right;">248</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Lamar County (13171)</td>
<td style="text-align: right;">246</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Carroll County (21041)</td>
<td style="text-align: right;">246</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Luna County (35029)</td>
<td style="text-align: right;">246</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Plymouth County (19149)</td>
<td style="text-align: right;">244</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Bienville Parish (22013)</td>
<td style="text-align: right;">243</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Sierra County (35051)</td>
<td style="text-align: right;">243</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Webster County (21233)</td>
<td style="text-align: right;">242</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Hardin County (19083)</td>
<td style="text-align: right;">241</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Morgan County (21175)</td>
<td style="text-align: right;">240</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Winn Parish (22127)</td>
<td style="text-align: right;">240</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Dade County (13083)</td>
<td style="text-align: right;">239</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Greene County (13133)</td>
<td style="text-align: right;">239</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Dickinson County (19059)</td>
<td style="text-align: right;">239</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Caldwell County (21033)</td>
<td style="text-align: right;">239</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Rabun County (13241)</td>
<td style="text-align: right;">237</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Union County (21225)</td>
<td style="text-align: right;">237</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Claiborne Parish (22027)</td>
<td style="text-align: right;">237</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Jefferson County (13163)</td>
<td style="text-align: right;">235</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Mariposa County (06043)</td>
<td style="text-align: right;">233</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Washington County (19183)</td>
<td style="text-align: right;">231</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Brooks County (13027)</td>
<td style="text-align: right;">230</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Cedar County (19031)</td>
<td style="text-align: right;">229</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Oconee County (13219)</td>
<td style="text-align: right;">228</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: St. James Parish (22093)</td>
<td style="text-align: right;">228</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Magoffin County (21153)</td>
<td style="text-align: right;">226</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Appling County (13001)</td>
<td style="text-align: right;">224</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Larue County (21123)</td>
<td style="text-align: right;">224</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Trinity County (06105)</td>
<td style="text-align: right;">223</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Banks County (13011)</td>
<td style="text-align: right;">222</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Harrison County (19085)</td>
<td style="text-align: right;">222</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Bath County (21011)</td>
<td style="text-align: right;">222</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Spencer County (21215)</td>
<td style="text-align: right;">222</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Tooele County (49045)</td>
<td style="text-align: right;">222</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Hamilton County (19079)</td>
<td style="text-align: right;">219</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Cook County (13075)</td>
<td style="text-align: right;">218</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Poweshiek County (19157)</td>
<td style="text-align: right;">218</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: La Salle Parish (22059)</td>
<td style="text-align: right;">217</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Monroe County (21171)</td>
<td style="text-align: right;">216</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Taos County (35055)</td>
<td style="text-align: right;">216</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Livingston County (21139)</td>
<td style="text-align: right;">215</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Fleming County (21069)</td>
<td style="text-align: right;">214</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Lincoln County (35027)</td>
<td style="text-align: right;">214</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Lassen County (06035)</td>
<td style="text-align: right;">210</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Screven County (13251)</td>
<td style="text-align: right;">210</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Appanoose County (19007)</td>
<td style="text-align: right;">210</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Bremer County (19017)</td>
<td style="text-align: right;">210</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Tama County (19171)</td>
<td style="text-align: right;">209</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Metcalfe County (21169)</td>
<td style="text-align: right;">209</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Owen County (21187)</td>
<td style="text-align: right;">208</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Clayton County (19043)</td>
<td style="text-align: right;">207</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Todd County (21219)</td>
<td style="text-align: right;">207</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: McLean County (21149)</td>
<td style="text-align: right;">206</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Towns County (13281)</td>
<td style="text-align: right;">205</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Clinton County (21053)</td>
<td style="text-align: right;">203</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Pike County (13231)</td>
<td style="text-align: right;">202</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Heard County (13149)</td>
<td style="text-align: right;">201</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Morgan County (13211)</td>
<td style="text-align: right;">201</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: McIntosh County (13191)</td>
<td style="text-align: right;">200</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Clay County (19041)</td>
<td style="text-align: right;">199</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Kossuth County (19109)</td>
<td style="text-align: right;">198</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Inyo County (06027)</td>
<td style="text-align: right;">197</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Rio Arriba County (35039)</td>
<td style="text-align: right;">194</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Floyd County (19067)</td>
<td style="text-align: right;">193</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Mills County (19129)</td>
<td style="text-align: right;">193</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Green County (21087)</td>
<td style="text-align: right;">193</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: West Feliciana Parish (22125)</td>
<td style="text-align: right;">191</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: San Miguel County (35047)</td>
<td style="text-align: right;">189</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Butler County (19023)</td>
<td style="text-align: right;">187</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Iron County (49021)</td>
<td style="text-align: right;">187</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Jeff Davis County (13161)</td>
<td style="text-align: right;">186</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Cass County (19029)</td>
<td style="text-align: right;">186</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Iowa County (19095)</td>
<td style="text-align: right;">181</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Delaware County (19055)</td>
<td style="text-align: right;">179</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Sioux County (19167)</td>
<td style="text-align: right;">178</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Caldwell Parish (22021)</td>
<td style="text-align: right;">177</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Union County (19175)</td>
<td style="text-align: right;">176</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Crittenden County (21055)</td>
<td style="text-align: right;">176</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Oglethorpe County (13221)</td>
<td style="text-align: right;">175</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: OBrien County (19141)</td>
<td style="text-align: right;">175</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Wolfe County (21237)</td>
<td style="text-align: right;">175</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: West Carroll Parish (22123)</td>
<td style="text-align: right;">175</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">UT: Cache County (49005)</td>
<td style="text-align: right;">175</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Colusa County (06011)</td>
<td style="text-align: right;">174</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Madison County (19121)</td>
<td style="text-align: right;">171</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Gallatin County (21077)</td>
<td style="text-align: right;">170</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Torrance County (35057)</td>
<td style="text-align: right;">169</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Cibola County (35006) - 1982+</td>
<td style="text-align: right;">168</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Jasper County (13159)</td>
<td style="text-align: right;">167</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Lyon County (21143)</td>
<td style="text-align: right;">167</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Wright County (19197)</td>
<td style="text-align: right;">166</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Buena Vista County (19021)</td>
<td style="text-align: right;">164</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Macon County (13193)</td>
<td style="text-align: right;">163</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Allamakee County (19005)</td>
<td style="text-align: right;">163</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Bracken County (21023)</td>
<td style="text-align: right;">162</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Bleckley County (13023)</td>
<td style="text-align: right;">161</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Wilkinson County (13319)</td>
<td style="text-align: right;">160</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Lee County (21129)</td>
<td style="text-align: right;">160</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Crawford County (19047)</td>
<td style="text-align: right;">159</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Terrell County (13273)</td>
<td style="text-align: right;">158</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Twiggs County (13289)</td>
<td style="text-align: right;">158</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Louisa County (19115)</td>
<td style="text-align: right;">156</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Shelby County (19165)</td>
<td style="text-align: right;">156</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Wilkes County (13317)</td>
<td style="text-align: right;">155</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Washington County (21229)</td>
<td style="text-align: right;">155</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Telfair County (13271)</td>
<td style="text-align: right;">153</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Jefferson County (19101)</td>
<td style="text-align: right;">153</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Roosevelt County (35041)</td>
<td style="text-align: right;">153</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Lincoln County (13181)</td>
<td style="text-align: right;">152</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Chickasaw County (19037)</td>
<td style="text-align: right;">152</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Winneshiek County (19191)</td>
<td style="text-align: right;">152</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">WA: San Juan County (53055)</td>
<td style="text-align: right;">152</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Greene County (19073)</td>
<td style="text-align: right;">151</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Cherokee County (19035)</td>
<td style="text-align: right;">150</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Guthrie County (19077)</td>
<td style="text-align: right;">148</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Keokuk County (19107)</td>
<td style="text-align: right;">148</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Montgomery County (19137)</td>
<td style="text-align: right;">147</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Monona County (19133)</td>
<td style="text-align: right;">146</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Grundy County (19075)</td>
<td style="text-align: right;">145</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Catahoula Parish (22025)</td>
<td style="text-align: right;">145</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Bacon County (13005)</td>
<td style="text-align: right;">144</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Trimble County (21223)</td>
<td style="text-align: right;">144</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Ballard County (21007)</td>
<td style="text-align: right;">143</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Calhoun County (19025)</td>
<td style="text-align: right;">142</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: McKinley County (35031)</td>
<td style="text-align: right;">142</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Evans County (13109)</td>
<td style="text-align: right;">140</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: St. Helena Parish (22091)</td>
<td style="text-align: right;">140</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Box Elder County (49003)</td>
<td style="text-align: right;">140</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">UT: Uintah County (49047)</td>
<td style="text-align: right;">140</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Carbon County (49007)</td>
<td style="text-align: right;">139</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Irwin County (13155)</td>
<td style="text-align: right;">138</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Lanier County (13173)</td>
<td style="text-align: right;">137</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Madison Parish (22065)</td>
<td style="text-align: right;">137</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Charlton County (13049)</td>
<td style="text-align: right;">136</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Emmet County (19063)</td>
<td style="text-align: right;">136</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Humboldt County (19091)</td>
<td style="text-align: right;">136</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Dooly County (13093)</td>
<td style="text-align: right;">133</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Turner County (13287)</td>
<td style="text-align: right;">133</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Hancock County (21091)</td>
<td style="text-align: right;">133</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Clarke County (19039)</td>
<td style="text-align: right;">132</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Palo Alto County (19147)</td>
<td style="text-align: right;">132</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Winnebago County (19189)</td>
<td style="text-align: right;">132</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Candler County (13043)</td>
<td style="text-align: right;">130</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Hancock County (19081)</td>
<td style="text-align: right;">130</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Van Buren County (19177)</td>
<td style="text-align: right;">130</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Menifee County (21165)</td>
<td style="text-align: right;">129</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Owsley County (21189)</td>
<td style="text-align: right;">129</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Early County (13099)</td>
<td style="text-align: right;">128</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Pulaski County (13235)</td>
<td style="text-align: right;">127</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Monroe County (19135)</td>
<td style="text-align: right;">127</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Franklin County (19069)</td>
<td style="text-align: right;">126</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Cumberland County (21057)</td>
<td style="text-align: right;">124</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Taylor County (13269)</td>
<td style="text-align: right;">123</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Fremont County (19071)</td>
<td style="text-align: right;">123</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Sac County (19161)</td>
<td style="text-align: right;">123</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Fulton County (21075)</td>
<td style="text-align: right;">123</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Hancock County (13141)</td>
<td style="text-align: right;">121</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">KY: Elliott County (21063)</td>
<td style="text-align: right;">119</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Long County (13183)</td>
<td style="text-align: right;">118</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Seminole County (13253)</td>
<td style="text-align: right;">118</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Red River Parish (22081)</td>
<td style="text-align: right;">117</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Quay County (35037)</td>
<td style="text-align: right;">117</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Socorro County (35053)</td>
<td style="text-align: right;">117</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Johnson County (13167)</td>
<td style="text-align: right;">116</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">UT: Sevier County (49041)</td>
<td style="text-align: right;">116</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Adair County (19001)</td>
<td style="text-align: right;">115</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Nicholas County (21181)</td>
<td style="text-align: right;">115</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Sanpete County (49039)</td>
<td style="text-align: right;">114</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Miller County (13201)</td>
<td style="text-align: right;">113</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Lucas County (19117)</td>
<td style="text-align: right;">113</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Jenkins County (13165)</td>
<td style="text-align: right;">112</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Marion County (13197)</td>
<td style="text-align: right;">112</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Wayne County (19185)</td>
<td style="text-align: right;">112</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Mitchell County (19131)</td>
<td style="text-align: right;">110</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Montgomery County (13209)</td>
<td style="text-align: right;">109</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Wilcox County (13315)</td>
<td style="text-align: right;">107</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Carlisle County (21039)</td>
<td style="text-align: right;">107</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Clinch County (13065)</td>
<td style="text-align: right;">105</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Lyon County (19119)</td>
<td style="text-align: right;">104</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Warren County (13301)</td>
<td style="text-align: right;">103</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">UT: Duchesne County (49013)</td>
<td style="text-align: right;">103</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Modoc County (06049)</td>
<td style="text-align: right;">101</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Decatur County (19053)</td>
<td style="text-align: right;">101</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Randolph County (13243)</td>
<td style="text-align: right;">100</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Pocahontas County (19151)</td>
<td style="text-align: right;">100</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: Cameron Parish (22023)</td>
<td style="text-align: right;">98</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Colfax County (35007)</td>
<td style="text-align: right;">97</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA: East Carroll Parish (22035)</td>
<td style="text-align: right;">95</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">UT: Summit County (49043)</td>
<td style="text-align: right;">94</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Howard County (19089)</td>
<td style="text-align: right;">93</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Worth County (19195)</td>
<td style="text-align: right;">93</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Treutlen County (13283)</td>
<td style="text-align: right;">92</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Hickman County (21105)</td>
<td style="text-align: right;">91</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Davis County (19051)</td>
<td style="text-align: right;">90</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Los Alamos County (35028)</td>
<td style="text-align: right;">90</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Ida County (19093)</td>
<td style="text-align: right;">87</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">LA: Tensas Parish (22107)</td>
<td style="text-align: right;">87</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Atkinson County (13003)</td>
<td style="text-align: right;">85</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Talbot County (13263)</td>
<td style="text-align: right;">84</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Ringgold County (19159)</td>
<td style="text-align: right;">84</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Taylor County (19173)</td>
<td style="text-align: right;">78</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Wasatch County (49051)</td>
<td style="text-align: right;">76</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Osceola County (19143)</td>
<td style="text-align: right;">73</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Grand County (49019)</td>
<td style="text-align: right;">72</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Wheeler County (13309)</td>
<td style="text-align: right;">69</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">IA: Audubon County (19009)</td>
<td style="text-align: right;">66</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Stewart County (13259)</td>
<td style="text-align: right;">65</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Calhoun County (13037)</td>
<td style="text-align: right;">62</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Quitman County (13239)</td>
<td style="text-align: right;">53</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Schley County (13249)</td>
<td style="text-align: right;">52</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA: Adams County (19003)</td>
<td style="text-align: right;">51</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Millard County (49027)</td>
<td style="text-align: right;">51</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Mono County (06051)</td>
<td style="text-align: right;">50</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Glascock County (13125)</td>
<td style="text-align: right;">50</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">UT: Emery County (49015)</td>
<td style="text-align: right;">49</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Kane County (49025)</td>
<td style="text-align: right;">49</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Baker County (13007)</td>
<td style="text-align: right;">48</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Chattahoochee County (13053)</td>
<td style="text-align: right;">45</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY: Robertson County (21201)</td>
<td style="text-align: right;">44</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Catron County (35003)</td>
<td style="text-align: right;">43</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">UT: San Juan County (49037)</td>
<td style="text-align: right;">43</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Echols County (13101)</td>
<td style="text-align: right;">41</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Unknown (35999)</td>
<td style="text-align: right;">40</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Beaver County (49001)</td>
<td style="text-align: right;">38</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Hidalgo County (35023)</td>
<td style="text-align: right;">37</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Guadalupe County (35019)</td>
<td style="text-align: right;">35</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Union County (35059)</td>
<td style="text-align: right;">34</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Juab County (49023)</td>
<td style="text-align: right;">33</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Clay County (13061)</td>
<td style="text-align: right;">32</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">GA: Webster County (13307)</td>
<td style="text-align: right;">31</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: De Baca County (35011)</td>
<td style="text-align: right;">31</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CA: Sierra County (06091)</td>
<td style="text-align: right;">30</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA: Taliaferro County (13265)</td>
<td style="text-align: right;">29</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM: Mora County (35033)</td>
<td style="text-align: right;">27</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">UT: Garfield County (49017)</td>
<td style="text-align: right;">27</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Morgan County (49029)</td>
<td style="text-align: right;">16</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">UT: Piute County (49031)</td>
<td style="text-align: right;">15</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Wayne County (49055)</td>
<td style="text-align: right;">14</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NJ: Unknown (34999)</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Daggett County (49009)</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">NM: Harding County (35021)</td>
<td style="text-align: right;">10</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT: Rich County (49033)</td>
<td style="text-align: right;">10</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">CA: Alpine County (06003)</td>
<td style="text-align: right;">7</td>
<td style="text-align: right;">0.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">HI: Kalawao County (15005) - 2000+</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">0.0</td>
</tr>
</tbody>
</table>

### States

    mydata_1 <- mydata_1 %>% mutate(state = substr(State.county, 1, 2))

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(state) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup() %>% arrange(desc(Count))

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">state</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">CA</td>
<td style="text-align: right;">250383</td>
<td style="text-align: right;">35.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">GA</td>
<td style="text-align: right;">93978</td>
<td style="text-align: right;">13.4</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NJ</td>
<td style="text-align: right;">86184</td>
<td style="text-align: right;">12.3</td>
</tr>
<tr class="even">
<td style="text-align: left;">KY</td>
<td style="text-align: right;">69863</td>
<td style="text-align: right;">9.9</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LA</td>
<td style="text-align: right;">53384</td>
<td style="text-align: right;">7.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">WA</td>
<td style="text-align: right;">40509</td>
<td style="text-align: right;">5.8</td>
</tr>
<tr class="odd">
<td style="text-align: left;">CT</td>
<td style="text-align: right;">39129</td>
<td style="text-align: right;">5.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">IA</td>
<td style="text-align: right;">34820</td>
<td style="text-align: right;">5.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">NM</td>
<td style="text-align: right;">13825</td>
<td style="text-align: right;">2.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">HI</td>
<td style="text-align: right;">11870</td>
<td style="text-align: right;">1.7</td>
</tr>
<tr class="odd">
<td style="text-align: left;">UT</td>
<td style="text-align: right;">9058</td>
<td style="text-align: right;">1.3</td>
</tr>
</tbody>
</table>

#### States grouping based on Temp

-   High Temp States: HI, LA, GA
-   Medium Temp States: CA, NM
-   Low Temp States: KY, NJ, CT, IA, UT

<!-- -->

    mydata_1 <- mydata_1 %>%
      mutate(state_T = case_when(
        state %in% c("HI", "LA", "GA") ~ "High Temp",
        state %in% c("CA", "NM") ~ "Medium Temp",
        state %in% c("KY", "NJ", "CT", "IA", "UT") ~ "Low Temp",
      ))

    # Create a summary table with counts and percentages
    summary_table <- mydata_1 %>%
      group_by(state_T) %>%
      summarise(
        Count = n(),  # Count of each category
        Percentage = round((n() / nrow(mydata_1)) * 100, 1)  # Percentage of each category
      ) %>% ungroup() %>% arrange(desc(Count))

    # Display the summary table
    kable(summary_table, caption = "")

<table>
<thead>
<tr class="header">
<th style="text-align: left;">state_T</th>
<th style="text-align: right;">Count</th>
<th style="text-align: right;">Percentage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Medium Temp</td>
<td style="text-align: right;">264208</td>
<td style="text-align: right;">37.6</td>
</tr>
<tr class="even">
<td style="text-align: left;">Low Temp</td>
<td style="text-align: right;">239054</td>
<td style="text-align: right;">34.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">High Temp</td>
<td style="text-align: right;">159232</td>
<td style="text-align: right;">22.7</td>
</tr>
<tr class="even">
<td style="text-align: left;">NA</td>
<td style="text-align: right;">40509</td>
<td style="text-align: right;">5.8</td>
</tr>
</tbody>
</table>

### Survival curves

#### Overall

    summary(mydata_1$Survival.months)  # Gives Min, 1st Qu., Median, Mean, 3rd Qu., Max

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##    0.00    2.00    9.00   25.58   28.00  263.00

    sd(mydata_1$Survival.months)       # Standard Deviation

    ## [1] 40.50034

    # Create a censoring variable: 1 if death occurred, 0 if censored (last follow-up)
    mydata_1 <- mydata_1 %>%
      mutate(status = ifelse(Vital.status.recode..study.cutoff.used. == "Dead", 1, 0))  # 1 = death, 0 = censored

    # Fit Kaplan-Meier survival model
    km_fit <- survfit(Surv(Survival.months, status) ~ 1, data = mydata_1)

    # Plot Kaplan-Meier survival curve overall
    ggsurvplot(km_fit,
               data = mydata_1,
               legend.title = "",
               xlab = "Overall survival (months)",
               ylab = "Overall survival (%)",
               title = "Overall Survival Among Patients With Lung Cancer",
               risk.table = TRUE,
               conf.int = FALSE,
               palette = c("red", "blue"),
               ggtheme = theme_minimal())

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-78-1.png)

#### by Sex

    # Set the levels of Sex in the desired order
    mydata_1$Sex <- factor(mydata_1$Sex, levels = c("Male", "Female"))

    # Fit Kaplan-Meier survival model, stratified by sex
    km_fit_sex <- survfit(Surv(Survival.months, status) ~ Sex, data = mydata_1)

    # Plot Kaplan-Meier survival curve by sex
    ggsurvplot(km_fit_sex,
               data = mydata_1,
               legend.title = "",   # Legend title for groups
               legend.labs = c("Male", "Female"),  # Customize legend labels
               xlab = "Overall survival (months)",   # X-axis label
               ylab = "Overall survival (%)",  # Y-axis label
               title = "Overall Survival Among Patients With Lung Cancer by Sex",  # Title
               risk.table = TRUE,  # Show the risk table below the plot
               risk.table.title = "",
               conf.int = FALSE,
               palette = c("red", "blue"),  # Set colors for male and female
               ggtheme = theme_minimal(),
               pval = TRUE, 
               pval.size = 4,
               pval.coord = c(20, 0.5),      
               surv.median.line = "hv")  # Set a minimal theme

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 2 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 2 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 2 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 2 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-79-1.png)

#### by Stage (“Distant”, “Localized”, “Regional”)

    # Subset the data to include only the desired stages
    mydata_1_filtered <- mydata_1[mydata_1$combined_stage %in% c("Distant", "Localized", "Regional"), ]

    # Set the levels of combined_stage in the desired order
    mydata_1_filtered$combined_stage <- factor(mydata_1_filtered$combined_stage,
                                              levels = c("Localized", "Regional", "Distant"))

    # Fit Kaplan-Meier survival model, stratified by combined stage
    km_fit_stage <- survfit(Surv(Survival.months, status) ~ combined_stage, data = mydata_1_filtered)

    # Plot Kaplan-Meier survival curve by stage
    ggsurvplot(km_fit_stage,
               data = mydata_1_filtered,
               legend.title = "",
               legend.labs = c("Localized", "Regional", "Distant"),  # Legend labels in the desired order
               xlab = "Overall survival (months)",
               ylab = "Overall survival (%)",
               title = "Overall Survival Among Patients With Lung Cancer by Stage at Diagnosis",  # Adjust title
               risk.table = TRUE,
               risk.table.title = "",
               conf.int = FALSE,
               palette = "Dark2",
               ggtheme = theme_minimal(),
               risk.table.fontsize = 2.5,
               risk.table.height = 0.25,
               pval = TRUE, 
               pval.size = 4,
               pval.coord = c(60, 0.6),      
               surv.median.line = "hv")

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-80-1.png)

#### by Stage (“Early stage (I-IIIA)”, “Late stage (IIIB-IV)”)

    # Subset the data to include only the desired stages
    mydata_1_filtered <- mydata_1[mydata_1$stage_binary %in% c("Early stage", "Late stage"), ]

    # Set the levels of combined_stage in the desired order
    mydata_1_filtered$stage_binary <- factor(mydata_1_filtered$stage_binary,
                                              levels = c("Early stage", "Late stage"))

    # Fit Kaplan-Meier survival model, stratified by combined stage
    km_fit_stage <- survfit(Surv(Survival.months, status) ~ stage_binary, data = mydata_1_filtered)

    # Plot Kaplan-Meier survival curve by stage
    ggsurvplot(km_fit_stage,
               data = mydata_1_filtered,
               legend.title = "",
               legend.labs = c("Early stage (I-IIIA)", "Late stage (IIIB-IV)"),  # Legend labels in the desired order
               xlab = "Overall survival (months)",
               ylab = "Overall survival (%)",
               title = "Overall Survival Among Patients With Lung Cancer by Stage at Diagnosis",  # Adjust title
               risk.table = TRUE,
               risk.table.title = "",
               conf.int = FALSE,
               palette = "Dark2",
               ggtheme = theme_minimal(),
               risk.table.fontsize = 2.5,
               risk.table.height = 0.25,
               pval = TRUE, 
               pval.size = 4,
               pval.coord = c(40, 0.6),      
               surv.median.line = "hv")

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 2 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 2 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 2 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 2 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-81-1.png)

#### by Race/Origin

    # Subset the data to include only the desired race/origin
    mydata_1_filtered <- mydata_1[mydata_1$Race.recode..White..Black..Other. %in% c("White", "Black", "Other (American Indian/AK Native, Asian/Pacific Islander)"), ]

    # Set the levels of Race.recode..White..Black..Other. in the desired order
    mydata_1_filtered$Race.recode..White..Black..Other. <- factor(mydata_1_filtered$Race.recode..White..Black..Other.,
                                              levels = c("White", "Black", "Other (American Indian/AK Native, Asian/Pacific Islander)"))

    # Fit Kaplan-Meier survival model, stratified by race/origin
    km_fit_race <- survfit(Surv(Survival.months, status) ~ Race.recode..White..Black..Other., data = mydata_1_filtered)

    # Plot Kaplan-Meier survival curve by race/origin
    ggsurvplot(km_fit_race,
               data = mydata_1_filtered,
               legend.title = "Race/origin",
               legend.labs = c("White", "Black", "Other"),  # Legend labels in the desired order
               xlab = "Overall survival (months)",
               ylab = "Overall survival (%)",
               title = "Overall Survival Among Patients With Lung Cancer by race/origin at Diagnosis",  # Adjust title
               risk.table = TRUE,
               risk.table.title = "",
               conf.int = FALSE,
               palette = "Dark2",
               ggtheme = theme_minimal(),
               risk.table.fontsize = 2.5,
               risk.table.height = 0.25,
               pval = TRUE, 
               pval.size = 4,
               pval.coord = c(20, 0.55),      
               surv.median.line = "hv")

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-82-1.png)

#### by Histological Type

    # Subset the data to include only the desired histological type
    mydata_1_filtered <- mydata_1[mydata_1$histological_type %in% c("Adenocarcinoma", "Squamous Cell Carcinoma", "Large Cell Carcinoma", "Small Cell Carcinoma"), ]

    # Set the levels of histological_type in the desired order
    mydata_1_filtered$histological_type <- factor(mydata_1_filtered$histological_type,
                                              levels = c("Adenocarcinoma", "Squamous Cell Carcinoma", "Large Cell Carcinoma", "Small Cell Carcinoma"))

    # Fit Kaplan-Meier survival model, stratified by histological_type
    km_fit_hs <- survfit(Surv(Survival.months, status) ~ histological_type, data = mydata_1_filtered)

    # Plot Kaplan-Meier survival curve by histological_type
    ggsurvplot(km_fit_hs,
               data = mydata_1_filtered,
               legend.title = "",
               legend.labs = c("Adenocarcinoma", "Squamous Cell Carcinoma", "Large Cell Carcinoma", "Small Cell Carcinoma"),  # Legend labels in the desired order
               xlab = "Overall survival (months)",
               ylab = "Overall survival (%)",
               title = "Overall Survival Among Patients With Lung Cancer by histological type",  # Adjust title
               risk.table = TRUE,
               risk.table.title = "",
               conf.int = FALSE,
               palette = "Dark2",
               ggtheme = theme_minimal(),
               risk.table.fontsize = 2.5,
               risk.table.height = 0.27,
               pval = TRUE, 
               pval.size = 4,
               pval.coord = c(20, 0.55),      
               surv.median.line = "hv")

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 4 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 4 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.
    ## All aesthetics have length 1, but the data has 4 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single row.

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 4 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-83-1.png)

#### by Stage and Year (Early/Late stage and Before 2015/After 2015)

    # Fit Kaplan-Meier survival model, stratified by Stage and Year
    km_fit_stage_year <- survfit(Surv(Survival.months, status) ~ stage_binary + year_2015, data = mydata_1)

    # Plot Kaplan-Meier survival curve by Stage and Year
    ggsurvplot(km_fit_stage_year,
               data = mydata_1,
               legend.title = "",
               legend.labs = c("Early Stage - After 2015", "Early Stage - Before 2015", "Late Stage - After 2015", "Late Stage - Before 2015"),  # Legend labels in the desired order
               xlab = "Overall survival (months)",
               ylab = "Overall survival (%)",
               title = "Overall Survival Among Patients With Lung Cancer by Stage and Year",  # Adjust title
               risk.table = TRUE,
               risk.table.title = "",
               conf.int = FALSE,
               palette = "Dark2",
               ggtheme = theme_minimal(),
               risk.table.fontsize = 2.5,
               risk.table.height = 0.28,
               pval = TRUE, 
               pval.size = 4,
               pval.coord = c(60, 0.6),      
               surv.median.line = "hv")

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 4 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 4 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 4 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 4 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-84-1.png)

#### by States (High/Medium/Low Temp)

    # Subset the data to include only the desired histological type
    mydata_1_filtered <- mydata_1[mydata_1$state_T %in% c("High Temp", "Medium Temp", "Low Temp"), ]

    # Set the levels of Temp in the desired order
    mydata_1_filtered$state_T <- factor(mydata_1_filtered$state_T,
                                              levels = c("High Temp", "Medium Temp", "Low Temp"))

    # Fit Kaplan-Meier survival model, stratified by Temp
    km_fit_temp <- survfit(Surv(Survival.months, status) ~ state_T, data = mydata_1_filtered)

    # Plot Kaplan-Meier survival curve by Temp
    ggsurvplot(km_fit_temp,
               data = mydata_1_filtered,
               legend.title = "",
               legend.labs = c("High Temp States", "Medium Temp States", "Low Temp States"),  # Legend labels in the desired order
               xlab = "Overall survival (months)",
               ylab = "Overall survival (%)",
               title = "Overall Survival Among Patients With Lung Cancer by Temp States",  # Adjust title
               risk.table = TRUE,
               risk.table.title = "",
               conf.int = FALSE,
               palette = "Dark2",
               ggtheme = theme_minimal(),
               risk.table.fontsize = 2.5,
               risk.table.height = 0.27,
               pval = TRUE, 
               pval.size = 4,
               pval.coord = c(20, 0.5),      
               surv.median.line = "hv")

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 3 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-85-1.png)

#### by Smoking Prevalence in county level

    mydata_1 <- mydata_1 %>% 
      mutate(smoking_prevalence = case_when(
        Year.of.diagnosis %in% c(2000:2003) ~ as.numeric(X..Current.Smoker..age.18....sae.2000.2003.) / 10000,
        Year.of.diagnosis %in% c(2004:2007) ~ as.numeric(X..Current.Smoker..age.18....sae.2004.2007.) / 10000,
        Year.of.diagnosis %in% c(2008:2010) ~ as.numeric(X..Current.Smoker..age.18....sae.2008.2010.) / 10000,
        Year.of.diagnosis %in% c(2011:2013) ~ as.numeric(X..Current.Smoker..age.18....sae.2011.2013.) / 10000,
        Year.of.diagnosis %in% c(2014:2016) ~ as.numeric(X..Current.Smoker..age.18....sae.2014.2016.) / 10000,
      )) %>% mutate(smoking_quintile = ntile(smoking_prevalence, 5))

    ## Warning: There were 5 warnings in `mutate()`.
    ## The first warning was:
    ## ℹ In argument: `smoking_prevalence = case_when(...)`.
    ## Caused by warning:
    ## ! NAs introduced by coercion
    ## ℹ Run `dplyr::last_dplyr_warnings()` to see the 4 remaining warnings.

    # Fit Kaplan-Meier survival model, stratified by Temp
    km_fit_smoking <- survfit(Surv(Survival.months, status) ~ smoking_quintile, data = mydata_1)

    # Customize the plot with highlighted quintiles 1 and 5, and dashed or grey for quintiles 2, 3, 4
    ggsurvplot(km_fit_smoking,
               data = mydata_1,
               legend.title = "",
               legend.labs = c("Quintile 1 (Low Smoking)", "Quintile 2", "Quintile 3", "Quintile 4", "Quintile 5 (High Smoking)"),  # Legend labels
               xlab = "Overall survival (months)",
               ylab = "Overall survival (%)",
               title = "Overall Survival Among Patients With Lung Cancer by Smoking Quintiles",
               risk.table = TRUE,
               risk.table.title = "",
               conf.int = FALSE,
               ggtheme = theme_minimal(),
               risk.table.fontsize = 2.5,
               risk.table.height = 0.27,
               pval = TRUE, 
               pval.size = 4,
               pval.coord = c(20, 0.55),      
               surv.median.line = "hv")

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 5 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 5 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 5 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 5 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-86-1.png)

#### by Yost Index (socioeconomic status (SES) index) in county level

    mydata_1 <- merge(mydata_1, mydata_Yost, by = c("State.county", "Year.of.diagnosis"), all.x = TRUE)

    mydata_1 <- mydata_1 %>% mutate(Yost_index = as.numeric(Yost.Index)) %>% mutate(Yost_index_quintile = ntile(Yost_index, 5)) %>% select(Patient.ID, Yost_index, Yost_index_quintile) %>% full_join(mydata_1, by = "Patient.ID")

    ## Warning: There was 1 warning in `mutate()`.
    ## ℹ In argument: `Yost_index = as.numeric(Yost.Index)`.
    ## Caused by warning:
    ## ! NAs introduced by coercion

    # Fit Kaplan-Meier survival model, stratified by Temp
    km_fit_yost <- survfit(Surv(Survival.months, status) ~ Yost_index_quintile, data = mydata_1)

    # Customize the plot with highlighted quintiles 1 and 5, and dashed or grey for quintiles 2, 3, 4
    ggsurvplot(km_fit_yost,
               data = mydata_1,
               legend.title = "",
               legend.labs = c("Quintile 1 (Low Yost Index)", "Quintile 2", "Quintile 3", "Quintile 4", "Quintile 5 (High Yost Index)"),  # Legend labels
               xlab = "Overall survival (months)",
               ylab = "Overall survival (%)",
               title = "Overall Survival Among Patients With Lung Cancer by Yost Index",
               risk.table = TRUE,
               risk.table.title = "",
               conf.int = FALSE,
               ggtheme = theme_minimal(),
               risk.table.fontsize = 2.5,
               risk.table.height = 0.3,
               pval = TRUE, 
               pval.size = 4,
               pval.coord = c(20, 0.55),      
               surv.median.line = "hv")

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 5 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.

    ## Warning in geom_segment(aes(x = 0, y = max(y2), xend = max(x1), yend = max(y2)), : All aesthetics have length 1, but the data has 5 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 5 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.
    ## All aesthetics have length 1, but the data has 5 rows.
    ## ℹ Please consider using `annotate()` or provide this layer with data containing a single
    ##   row.

![](Descriptive_analysis_files/figure-markdown_strict/unnamed-chunk-87-1.png)
