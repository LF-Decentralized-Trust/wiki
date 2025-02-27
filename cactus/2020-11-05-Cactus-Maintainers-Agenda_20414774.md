1. [Hyperledger Cacti](index.html)
2. [Hyperledger Cacti Home](Hyperledger-Cacti-Home_20414469.html)
3. [Meeting Agendas](Meeting-Agendas_20414488.html)
4. [2020 Agendas](2020-Agendas_20414504.html)

# Hyperledger Cacti : 2020-11-05 Cactus Maintainers Agenda

Created by Peter Somogyvari, last modified on Nov 04, 2020

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming community for all. For more information please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming community for all. For more information please visit our Code of Conduct: [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Discussion

1. USA Thanksgiving week maintainer's call (Nov 24th UTC)
   
   1. Peter is off
   2. Jonathan is off
2. **v0.2.0** release shout-out
3. Peter talks about the Cactus build system (Lerna/Webpack/Typescript)
   
   1. Package categories: 
      
      ![](attachments/20414774/20414776.png?height=250)
   2. Utility to view complete package dependency graph
      
      1. SVG format
         
         ```
         $ npx lerna-dependency-graph --outputFormat svg --outputPath ./cactus-package-dependency-graph.svg
         ```
         
         [package-dependency-graph.svg](attachments/20414774/20414780.svg)
      2. PDF format
         
         ```
         $ npx lerna-dependency-graph --outputFormat pdf --outputPath ./cactus-package-dependency-graph.pdf
         ```
         
         [package-dependency-graph.pdf](attachments/20414774/20414781.pdf)
4. Discussion on privacy-preserving Cactus interfaces.  We need a plan (and rigorous proofs) in order to properly build these.
5. CII Badge Completion
   
   1. [https://github.com/hyperledger/cactus/issues/357](https://github.com/hyperledger/cactus/issues/357)
6. Confirm **v0.3.0** milestone scope
7. Ad-hoc discussion items
8. PR grinder

## Attachments:

![](images/icons/bullet_blue.gif) [cactus-package-directory-hierarchy-2020-11-04 12-19-21.png](attachments/20414774/20414776.png) (image/png)  
![](images/icons/bullet_blue.gif) [package-dependency-graph.svg](attachments/20414774/20414780.svg) (image/svg+xml)  
![](images/icons/bullet_blue.gif) [package-dependency-graph.pdf](attachments/20414774/20414781.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 12:37

[Atlassian](http://www.atlassian.com/)
