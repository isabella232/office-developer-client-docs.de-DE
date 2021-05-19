---
title: Abschnitt "Formularkonfigurationsdatei" [Verben]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417784"
---
# <a name="form-configuration-file-verbs-section"></a>Abschnitt "Formularkonfigurationsdatei" [Verben]

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im **Abschnitt [Verben]** werden die vollständigen Verben aufgeführt, die vom Formular unterstützt werden. Das Format des **Abschnitts [Verben]** ist: 
  
 **[Verben]**
  
 **Verb1**  =   _string_
  
Im Folgenden finden Sie ein Beispiel für einen **[Verbs]-Abschnitt.** 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Jedes Verb ist in einem separaten **[Verb.** _string_ **]** section. A **[Verb.** _Im Abschnitt string_ **]** wird ein einzelnes Verb beschrieben, das vom Formular angeboten wird. Der **Eintrag DisplayName** in einem **[Verb.** _string_ **]** -Abschnitt gibt den Befehlsnamen an, der auf der Benutzeroberfläche angezeigt wird. Der **Code-Eintrag** entspricht der Verbnummer, die in der [IMAPIForm::D oVerb-Methode übergeben](imapiform-doverb.md) wird. Die Syntax für **das [Verb.** _string_ **]** section is: 
  
 **[Verb.** _string_ **]**
  
 **DisplayName**  =   _angezeigte Zeichenfolge_
  
 **Code**  =   _integer_
  
 **Flags**  =   _integer_
  
 **Attribs**  =   _integer_
  
Im Folgenden finden Sie ein Beispiel für **ein [Verb.** _string_ **]** section. 
  
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

In diesem Abschnitt aufgeführte Verben werden von einem Client mithilfe der [IMAPIFormInfo::CalcVerbSet-Methode abgerufen.](imapiforminfo-calcverbset.md) Verben werden aktiviert, indem die [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) des Formulars aufruft und die Codenummer des verb übergeben wird, das ausgeführt werden soll. 
  

