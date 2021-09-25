---
title: Abschnitt "Form Configuration File [Verbs]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9eb46f67d205d118c2eef77bd789cd76beff394
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556700"
---
# <a name="form-configuration-file-verbs-section"></a>Abschnitt "Form Configuration File [Verbs]

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Verbs]** listet den vollständigen Satz von Verben auf, die vom Formular unterstützt werden. Das Format des **[Verbs]-Abschnitts** lautet: 
  
 **[Verben]**
  
 **Verb1**  =   _zeichenfolge_
  
Es folgt ein Beispiel für einen **[Verbs]-Abschnitt.** 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Jedes Verb wird in einem separaten **[Verb.** _string_ **]** section. Ein **[Verb.** im Abschnitt string] wird ein einzelnes verb beschrieben, das vom Formular angeboten wird.   Der **DisplayName-Eintrag** in einem **[Verb.** _string]_  gibt den Befehlsnamen an, der auf der Benutzeroberfläche angezeigt wird. Der **Codeeintrag** entspricht der Verbnummer, die in der [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) übergeben wird. Die Syntax für **das [Verb.** _string_ **]** section is: 
  
 **[Verb.** _string_ **]**
  
 **DisplayName**  =   _angezeigte Zeichenfolge_
  
 **Code**  =   _ganze Zahl_
  
 **Flags**  =   _ganze Zahl_
  
 **Attribs**  =   _ganze Zahl_
  
Nachfolgend sehen Sie ein Beispiel für **ein [Verb.** _string_ **]** section. 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

Verben, die in diesem Abschnitt aufgeführt sind, werden von einem Client mithilfe der [IMAPIFormInfo::CalcVerbSet-Methode](imapiforminfo-calcverbset.md)abgerufen. Verben werden aktiviert, indem die [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) des Formulars aufgerufen und die Codenummer des auszuführenden Verbs übergeben wird. 
  

