---
title: Automatisieren von InfoPath aus einer externen Anwendung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath bietet Anwendungsautomatisierung aus Code, der mit COM und Skript geschrieben wurde, mithilfe von Methoden des Application-Objekts und der XDocuments-Auflistung.
ms.openlocfilehash: 8bd62af41ff4cc11a4768b1a054c2587081e6a53
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552129"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatisieren von InfoPath aus einer externen Anwendung

Microsoft InfoPath bietet Anwendungsautomatisierung aus Code, der mit COM und Skript geschrieben wurde, mithilfe von Methoden des **Application-Objekts** und der **XDocuments-Auflistung.** 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Übersicht über die Objekte Application und XDocument

Das **Application-Objekt** enthält die folgenden Methoden, die für die Automatisierung verwendet werden: 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|**CacheSolution** <br/> |Überprüft die Datei im Cache und aktualisiert sie ggf. vom veröffentlichten Speicherort der Formularvorlage.  <br/> |
|**Quit** <br/> |Beendet die Microsoft Office InfoPath-Anwendung.  <br/> |
|**RegisterSolution** <br/> |Installiert die angegebene Microsoft Office InfoPath-Formularvorlage.  <br/> |
|**UnregisterSolution** <br/> |Deinstalliert die angegebene Microsoft Office InfoPath-Formularvorlage.  <br/> |
   
Die **XDocuments-Auflistung** enthält die folgenden Methoden, die für die externe Automatisierung verwendet werden können: 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|**Close**-Methode  <br/> |Schließt das angegebene Microsoft Office InfoPath-Formular.  <br/> |
|**New-Methode**  <br/> |Erstellt ein neues Microsoft Office InfoPath-Formular.  <br/> |
|**NewFromSolution-Methode**  <br/> |Erstellt ein neues Microsoft Office InfoPath-Formulars basierend auf der angegebenen Formularvorlage.  <br/> |
|**NewFromSolutionWithData-Methode**  <br/> |Erstellt ein neues Microsoft Office InfoPath-Formular mithilfe der angegebenen XML-Daten und Formularvorlage.  <br/> |
|**Open-Methode**  <br/> |Öffnet das angegebene Microsoft Office InfoPath-Formular.  <br/> |
   
Um das **Application-Objekt** aus einer externen Anwendung zu verwenden, verwenden Sie die **CreateObject-Funktion** mit der ProgID der InfoPath-Anwendung ("InfoPath.Application"), um eine Objektvariable zu erstellen, die die InfoPath-Anwendung darstellt. Anschließend können Sie mit der **XDocuments-Eigenschaft** auf die **XDocuments-Auflistung** zugreifen und deren Methoden verwenden, um ein InfoPath-Formular zu öffnen oder zu erstellen. Im folgenden Beispiel wird die Erstellung eines Verweises auf das **Application-Objekt** mithilfe der Programmiersprache Microsoft Visual Basic 6.0 oder Visual Basic for Applications (VBA) veranschaulicht: 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Da die **CreateObject-Funktion** eine Objektvariable mit später Bindung erstellt, ist die automatische Anweisungsvervollständigung im Visual Basic-Editor nicht verfügbar. Informationen zur richtigen Aufrufsyntax finden Sie unter den Links in den vorherigen Tabellen. 
  

