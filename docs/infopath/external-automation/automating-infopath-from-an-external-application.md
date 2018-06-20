---
title: Automatisieren von InfoPath aus einer externen Anwendung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath bietet Anwendung Automatisierung von Code, COM und Skript mithilfe der Methoden des Application-Objekts und der XDocuments-Auflistung verwendet.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790626"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatisieren von InfoPath aus einer externen Anwendung

Microsoft InfoPath bietet Anwendung Automatisierung von Code, COM und Skript mithilfe der Methoden des **Application** -Objekts und der **XDocuments** -Auflistung verwendet. 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Übersicht über die Anwendung und der XDocument-Objekte

Das **Application** -Objekt enthält die folgenden Methoden, die für die Automatisierung verwendet: 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|**CacheSolution** <br/> |Untersucht die im Cache und, falls erforderlich, wird von den Veröffentlichungsort der Formularvorlage aktualisiert.  <br/> |
|**Quit** <br/> |Beendet die Anwendung Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Installiert die angegebene Microsoft Office InfoPath-Formularvorlage.  <br/> |
|**UnregisterSolution** <br/> |Deinstalliert die angegebene Microsoft Office InfoPath-Formularvorlage an.  <br/> |
   
Die **XDocuments** -Auflistung enthält die folgenden Methoden, die für die externe Automatisierung verwendet werden können: 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|**Close**-Methode  <br/> |Schließt das angegebene Microsoft Office InfoPath-Formular.  <br/> |
|**New** -Methode  <br/> |Erstellt ein neues Microsoft Office InfoPath-Formular.  <br/> |
|**NewFromSolution** -Methode  <br/> |Erstellt ein neues Microsoft Office InfoPath-Formular basierend auf der angegebenen Formularvorlage.  <br/> |
|**NewFromSolutionWithData** -Methode  <br/> |Erstellt ein neues Microsoft Office InfoPath-Formular mithilfe der angegebenen XML-Daten und der Formularvorlage.  <br/> |
|**Open** -Methode  <br/> |Öffnet das angegebene Microsoft Office InfoPath-Formular.  <br/> |
   
Um das **Application** -Objekt aus einer externen Anwendung verwenden möchten, verwenden Sie die **CreateObject** -Funktion mit die ProgID des InfoPath-Anwendung ("InfoPath.Application") um eine Objektvariable zu erstellen, die InfoPath-Anwendung darstellt. Sie können die **XDocuments** -Eigenschaft klicken Sie dann auf die **XDocuments** -Auflistung zuzugreifen und dessen Methoden zum Öffnen oder erstellen Sie ein InfoPath-Formular verwenden. Das folgende Beispiel veranschaulicht das Erstellen eines Verweises auf das **Application** -Objekt mithilfe der Microsoft Visual Basic 6.0 oder Visual Basic für Applikationen (VBA) Programmiersprache: 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Da eine Objektvariable späten Bindung mithilfe die **CreateObject** -Funktion erstellt wird, wird Abschluss der automatischen Anweisung in Visual Basic-Editor nicht verfügbar. Verweisen Sie auf die Links in den vorherigen Tabellen Informationen zur richtigen Aufrufsyntax. 
  

