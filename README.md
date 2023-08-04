# Connectedness-Analysis
TVP-VAR model developed by Antonakakis, N., Chatziantoniou, I., &amp; Gabauer, D.
#Antonakakis, N., Chatziantoniou, I., & Gabauer, D. (2020). Refined measures of dynamic connectedness based on time-varying parameter vector autoregressions. Journal of Risk and Financial Management, 13(4), 84.
dca = ConnectednessApproach(data, 
                            nlag=1, 
                            nfore=10,
                            window.size=200,
                            model="TVP-VAR",
                            connectedness="Time",
                            VAR_config=list(TVPVAR=list(kappa1=0.99, kappa2=0.96, prior="BayesPrior")))
PlotTCI(dca, ylim=c(0,40))
PlotTO(dca, ylim=c(0,60))
PlotFROM(dca, ylim=c(0,60))
PlotNET(dca, ylim=c(-30,30))
PlotNPDC(dca, ylim=c(-20,20))
PlotPCI(dca)
PlotNPT(dca)
PlotINF(dca, ylim=c(0,100))
PlotNetwork(dca, method="NPDC")
PlotNetwork(dca, method="PCI")
