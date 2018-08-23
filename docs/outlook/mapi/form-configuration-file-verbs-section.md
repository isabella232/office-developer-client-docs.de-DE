---
title: Abschnitt [Verbs] in der Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6a06283e3eb072e1f502d0b1bd303ce9f0733578
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583974"
---
# <a name="form-configuration-file-verbs-section"></a>Abschnitt [Verbs] in der Formularkonfigurationsdatei

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Im Abschnitt **[Verben]** wird der vollständige Satz von Verben, die vom Formular unterstützt. Das Format des Abschnitts **[Verben]** lautet: 
  
 **[Verben]**
  
 **Verb1** =  _Zeichenfolge_
  
Es folgt ein Beispiel für einen Abschnitt **[Verben]** . 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Jedes Verb definiert, in einer separaten **[Verb.** _Zeichenfolge_ **]** Abschnitt. Eine **[Verb.** _Zeichenfolge_ **]** Abschnitt beschreibt ein einzelnes Verb vom Formular angeboten. Der Eintrag " **DisplayName** " in einem **[Verb.** _Zeichenfolge_ Abschnitt **]** gibt den Namen des Befehls in der Benutzeroberfläche angezeigt. Der **Code** -Eintrag entspricht der Verbanzahl in der [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode übergeben. Die Syntax für die **[Verb.** _Zeichenfolge_ **]** Abschnitt ist: 
  
 **[Verb.** _Zeichenfolge_ **]**
  
 **DisplayName** =  _Zeichenfolge angezeigt_
  
 **Code** =  _ganze Zahl_
  
 **Flags** =  _ganze Zahl_
  
 **Attributen** =  _ganze Zahl_
  
Nachfolgend sehen Sie ein Beispiel für eine **[Verb.** _Zeichenfolge_ **]** Abschnitt. 
  
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

In diesem Abschnitt aufgeführten Verben werden von einem Client mithilfe der [Methode IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)abgerufen. Verben aktiviert sind, indem das Formular [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode aufrufen, und übergeben sie die Anzahl von Code für die auszuführende Aktion ausgeführt werden. 
  

