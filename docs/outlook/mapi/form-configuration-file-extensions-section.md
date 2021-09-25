---
title: Abschnitt "Form Configuration File [Extensions]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f3ffce0753ef62d8e61f9c6df010882d5bb5178
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587986"
---
# <a name="form-configuration-file-extensions-section"></a>Abschnitt "Form Configuration File [Extensions]

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Erweiterungen]** listet die erweiterten Attribute des Formulars auf, in der Regel ein benannter Eigenschaftensatz. Dabei handelt es sich um alle Attribute, die über die im Abschnitt **[Beschreibung]** der Formularkonfigurationsdatei aufgeführten Attribute hinausgehen. Erweiterte Attribute sind Eigenschaften, die von Aufrufen der **GetProps-Methode** des **IMAPIFormInfo-Objekts** zurückgegeben werden, wobei der High-Bit-Wert im Eigenschaftentag festgelegt ist. Clientanwendungen können die erweiterten Attribute eines Formulars ermitteln, indem sie diese Tags abrufen. Dazu rufen Clients die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) auf, übergeben die Namen der Eigenschaften des Formulars und rufen die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) auf, um die Eigenschaften abzurufen. 
  
 **[Erweiterungen]**
  
 **Erweiterung.** _string1_  =   _string2_
  
Jeder Abschnitt der Erweiterungseigenschaft definiert ein Erweiterungsattribut mithilfe der MAPI-Syntax der benannten Eigenschaft. Der Eigenschaftentyp muss entweder PT_LONG oder PT_STRING8 sein. Eigenschaftensätze, die benannte Zeichenfolgen enthalten, werden nicht unterstützt. Das Format des **[Extension]-Abschnitts** lautet: 
  
 **[Erweiterung.** _string2_ **]**
  
 **Typ**  =   _ganze Zahl_
  
 **NmidPropset**  =   _GUID_
  
 **NmidInteger**  =   _ganze Zahl_
  
 **Wert**  =   _zeichenfolge_  |   _ganze Zahl_
  
Nachfolgend finden Sie ein Beispiel für einen **[Extensions]-Abschnitt** und einen nachfolgenden verwandten Abschnitt. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


