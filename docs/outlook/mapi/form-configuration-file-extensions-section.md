---
title: Abschnitt "Formular Konfigurationsdatei [Erweiterungen]"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327300"
---
# <a name="form-configuration-file-extensions-section"></a>Abschnitt "Formular Konfigurationsdatei [Erweiterungen]"

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im Abschnitt **[Extensions]** werden die erweiterten Attribute des Formulars aufgelistet, in der Regel ein benannter Eigenschaftensatz, bei dem es sich nicht um die grundlegenden Attribute handelt, die im Abschnitt **[Beschreibung]** der Formular Konfigurationsdatei aufgeführt sind. Erweiterte Attribute sind Eigenschaften, die von Aufrufen der **** GetProps-Methode des **IMAPIFormInfo** -Objekts zurückgegeben werden, wobei das High-Bit im Property-Tag festgelegt ist. Client Anwendungen können die erweiterten Attribute eines Formulars bestimmen, sofern vorhanden, indem Sie diese Tags abrufen. Dazu rufen die Clients die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode auf, übergeben die Namen der Eigenschaften des Formulars und rufen die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode auf, um die Eigenschaften abzurufen. 
  
 **Erweiterungen**
  
 **Erweiterung.** _string1_ =  _string2_
  
Jeder Abschnitt der Extension-Eigenschaft definiert ein Erweiterungsattribut mit der Syntax der MAPI-Eigenschaft. Der Eigenschaftentyp muss entweder PT_LONG oder PT_STRING8 sein. Eigenschaftensätze mit benannten Zeichenfolgen werden nicht unterstützt. Das Format des Abschnitts **[Extension]** lautet: 
  
 **Erweiterung.** _string2_ **]**
  
 **Typ** =  _Integer_
  
 **NmidPropset** =  -_GUID_
  
 **NmidInteger** =  -_Ganzzahl_
  
 **Wert** =  __ String |  _Integer_
  
Es folgt ein Beispiel für einen **[Extensions]** -Abschnitt und einen nachfolgenden verwandten Abschnitt. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


