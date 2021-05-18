---
title: Automatisieren von InfoPath aus einer externen Anwendung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath bietet Anwendungsautomatisierung von Code, der mithilfe von COM und Skript mithilfe von Methoden des Application-Objekts und der XDocuments-Auflistung geschrieben wurde.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412667"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatisieren von InfoPath aus einer externen Anwendung

Microsoft InfoPath bietet Anwendungsautomatisierung von Code, der mithilfe von COM und Skript mithilfe von Methoden des **Application-Objekts** und der **XDocuments-Auflistung geschrieben** wurde. 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Übersicht über die Anwendungs- und XDocument-Objekte

Das **Application-Objekt** enthält die folgenden Methoden, die für die Automatisierung verwendet werden: 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|**CacheSolution** <br/> |Untersucht den im Cache und aktualisiert ihn bei Bedarf vom veröffentlichten Speicherort der Formularvorlage.  <br/> |
|**Quit** <br/> |Beendet die Microsoft Office InfoPath-Anwendung.  <br/> |
|**RegisterSolution** <br/> |Installiert die angegebene Microsoft Office InfoPath-Formularvorlage.  <br/> |
|**UnregisterSolution** <br/> |Deinstalliert die angegebene Microsoft Office InfoPath-Formularvorlage.  <br/> |
   
Die **XDocuments-Auflistung** enthält die folgenden Methoden, die für die externe Automatisierung verwendet werden können: 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|**Close**-Methode  <br/> |Schließt das angegebene Microsoft Office InfoPath-Formular.  <br/> |
|**Neue** Methode  <br/> |Erstellt ein neues Microsoft Office InfoPath-Formular.  <br/> |
|**NewFromSolution-Methode**  <br/> |Erstellt ein neues Microsoft Office InfoPath-Formular basierend auf der angegebenen Formularvorlage.  <br/> |
|**NewFromSolutionWithData-Methode**  <br/> |Erstellt ein neues Microsoft Office InfoPath-Formular mithilfe der angegebenen XML-Daten und Formularvorlage.  <br/> |
|**Open-Methode**  <br/> |Öffnet das angegebene Microsoft Office InfoPath-Formular.  <br/> |
   
Um das **Application-Objekt** aus einer externen Anwendung zu verwenden, verwenden Sie die **CreateObject-Funktion** mit der ProgID der InfoPath-Anwendung ("InfoPath.Application"), um eine Objektvariable zu erstellen, die die InfoPath-Anwendung darstellt. Anschließend können Sie die **XDocuments-Eigenschaft** verwenden, um auf die **XDocuments-Auflistung** zu zugreifen und die Methoden zum Öffnen oder Erstellen eines InfoPath-Formulars zu verwenden. Im folgenden Beispiel wird die Erstellung eines Verweises auf das **Application-Objekt** mithilfe der Programmiersprache Microsoft Visual Basic 6.0 oder Visual Basic for Applications (VBA) veranschaulicht: 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Da die **CreateObject-Funktion** eine Objektvariable mit später Bindung erstellt, steht der automatische Abschluss der Anweisung im Editor Visual Basic zur Verfügung. Informationen zur richtigen Aufrufsyntax finden Sie in den Links in den vorherigen Tabellen. 
  

