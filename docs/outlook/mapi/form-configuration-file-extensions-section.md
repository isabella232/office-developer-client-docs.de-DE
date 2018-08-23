---
title: Abschnitt [Extensions] in der Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 459c5f5a34421583141028cd9accad5e242d31ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573558"
---
# <a name="form-configuration-file-extensions-section"></a>Abschnitt [Extensions] in der Formularkonfigurationsdatei

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Extensions]** Listet die erweiterten Attribute des Formulars, in der Regel eine benannte Eigenschaft festgelegt, die alle außer den grundlegenden in den Abschnitt **[Beschreibung]** der Konfigurationsdatei Formular aufgeführten Attribute sind. Erweiterte Attribute sind Eigenschaften von Aufrufe der **GetProps** -Methode des **IMAPIFormInfo** -Objekts zurückgegeben wird, mit dem hohe Bit in das Eigenschafts-Tag festgelegt. Clientanwendungen können erweiterte Attribute eines Formulars, gegebenenfalls durch diese Tags abrufen bestimmen. Dazu Clients rufen Sie die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode und die Namen der Eigenschaften des Formulars übergeben, und rufen die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, um die Eigenschaften abzurufen. 
  
 **[Extensions]**
  
 **Erweiterung.** _String1_ =  _string2_
  
Jede Erweiterung-Eigenschaft im Abschnitt definiert eine von der mit dem Namen Eigenschaftensyntax MAPI Extension-Attribut. Der Eigenschaftentyp muss PT_LONG oder PT_STRING8. Eigenschaftensätze, die benannte Zeichenfolgen enthält, werden nicht unterstützt. Das Format des Abschnitts **[Erweiterung]** lautet: 
  
 **[Erweiterung.** _Zeichenfolge2_ **]**
  
 **Typ** =  _ganze Zahl_
  
 **NmidPropset** =  _Guid_
  
 **NmidInteger** =  _ganze Zahl_
  
 **Wert** =  _Zeichenfolge_ |  _ganze Zahl_
  
Ein Beispiel für einen Abschnitt **[Extensions]** und einer der folgenden Verwandte Abschnitte wird nach angezeigt. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


