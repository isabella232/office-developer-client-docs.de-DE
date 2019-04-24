---
title: Formular Konfigurationsdatei [Verbs] Abschnitt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327496"
---
# <a name="form-configuration-file-verbs-section"></a>Formular Konfigurationsdatei [Verbs] Abschnitt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Verbs]** enthält die vollständigen Verben, die vom Formular unterstützt werden. Das Format des Abschnitts **[Verbs]** lautet: 
  
 **Verben**
  
 **Verb1** =  -_Zeichenfolge_
  
Es folgt ein Beispiel für einen Abschnitt **[Verbs]** . 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Jedes Verb wird in einem separaten **[Verb.** _Zeichenfolge_ **]** -Abschnitt. Ein **[Verb.** _Zeichenfolge_ **]** section beschreibt ein einzelnes Verb, das vom Formular angeboten wird. Der Eintrag **DisplayName** in einem **[Verb.** _Zeichenfolge_ **]** -Abschnitt gibt den in der Benutzeroberfläche angezeigten Befehlsnamen an. Der **Code** Eintrag entspricht der Verb Nummer, die in der [IMAPIForm::D overb](imapiform-doverb.md) -Methode übergeben wird. Die Syntax für das **[Verb.** _Zeichenfolge_ **]** section ist: 
  
 **Verb.** _Zeichenfolge_ **]**
  
 **** Angezeigte Zeichen_Folge_  =  
  
 **Code** =  _Ganzzahl_
  
 **Flags** =  -_Ganzzahl_
  
 **Attribute** =  -_Ganzzahl_
  
Es folgt ein Beispiel für ein **[Verb.** _Zeichenfolge_ **]** -Abschnitt. 
  
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

Verben, die in diesem Abschnitt aufgelistet werden, werden von einem Client mithilfe der [IMAPIFormInfo:: CalcVerbSet-Methode](imapiforminfo-calcverbset.md)abgerufen. Verben werden aktiviert, indem die [IMAPIForm::D overb](imapiform-doverb.md) -Methode des Formulars aufgerufen und die Codenummer des auszuführenden Verbs übergeben wird. 
  

