---
title: Abschnitt "Formularkonfigurationsdatei [ Erweiterungen]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423755"
---
# <a name="form-configuration-file-extensions-section"></a>Abschnitt "Formularkonfigurationsdatei [ Erweiterungen]

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im **Abschnitt [Extensions]** werden die erweiterten Attribute des Formulars aufgelistet, in der Regel ein benannter Eigenschaftensatz, bei dem es sich um Attribute handelt, die über die grundlegenden Attribute hinausgehen, die im **Abschnitt [Beschreibung]** der Formularkonfigurationsdatei aufgeführt sind. Erweiterte Attribute sind Eigenschaften, die von Aufrufen an die **GetProps-Methode** des **IMAPIFormInfo-Objekts** zurückgegeben werden, deren High-Bit im Eigenschaftstag festgelegt ist. Clientanwendungen können die erweiterten Attribute eines Formulars bestimmen, sofern dies der Fall ist, indem diese Tags abgerufen werden. Dazu rufen Clients die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) auf, übergeben die Namen der Eigenschaften des Formulars und rufen die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) auf, um die Eigenschaften zu erhalten. 
  
 **[Erweiterungen]**
  
 **Erweiterung.** _string1_  =   _string2_
  
Jeder Abschnitt der Erweiterungseigenschaft definiert ein Erweiterungsattribut mithilfe der SYNTAX der benannten MAPI-Eigenschaft. Der Eigenschaftentyp muss entweder PT_LONG oder PT_STRING8. Eigenschaftssätze, die benannte Zeichenfolgen enthalten, werden nicht unterstützt. Das Format des **Abschnitts [Extension]** ist: 
  
 **[Erweiterung.** _string2_ **]**
  
 **Type**  =   _integer_
  
 **NmidPropset**  =   _guid_
  
 **NmidInteger**  =   _integer_
  
 **Wert**  =   _string_  |   _integer_
  
Nachfolgend finden Sie ein Beispiel für einen **Abschnitt [Extensions]** und einen nachfolgenden verwandten Abschnitt. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


