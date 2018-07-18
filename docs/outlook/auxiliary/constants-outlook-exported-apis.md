---
title: Konstanten (Outlook exportierter APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Dieses Thema enthält Konstantendefinitionen für APIs, die Outlook exportiert.
ms.openlocfilehash: 54b491e436b7b9275a227de40439ddb66d8d0c5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790927"
---
# <a name="constants-outlook-exported-apis"></a>Konstanten (Outlook exportierter APIs)

Dieses Thema enthält Konstantendefinitionen für APIs, die Outlook exportiert.
  
## <a name="definitions-for-time-zone-support"></a>Unterstützung von Definitionen für Zeitzone

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Unterstützung von Definitionen für Kategorie

|**Konstante**|**Definition**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Sonstige Versendung-IDs

Outlook macht die folgenden Versendung-IDs (Dispids) verfügbar, sodass Entwickler [IDispatch:: Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) verwenden können, um Zugriff auf die entsprechende Eigenschaft oder Methode oder die entsprechenden Ereignis überwachen. 
  
|**Zugehörige Konstante**|**DISPID-Wert**|**Beschreibung**|**Zutreffend-Schnittstelle**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Zum Aufrufen der entsprechenden Eigenschaft für ein Element wird überprüft, ob das Element wurde geändert, aber nicht gespeichert wurde verwendet.  <br/> |Objekte auf Elementebene  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Verwendet, um die entsprechende Methode in der Explorer oder Inspektor, um anzugeben, ob das Bild eines Kontakts, basierend auf einer bestimmten Argument anzeigen aufzurufen.  <br/> |Explorer oder Inspektor  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Verwendet, um die Ereignisbehandlung aus der **IDispatch:: Invoke** -Funktion, die vor einem Druckvorgang ausgelöst.  <br/> |Anwendung  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Verwendet, um die Ereignisbehandlung aus der **IDispatch:: Invoke** -Funktion, die ausgelöst wird, wenn Outlook abgeschlossen ist, lesen die Eigenschaften des Elements.  <br/> |Objekte auf Elementebene  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Aus Outlook exportierte APIs](outlook-exported-apis.md)
- [Informationen zu von Outlook exportierten APIs](about-apis-exported-by-outlook.md)
- [Bestimmen Sie, ob ein Outlook-Element geändert, jedoch nicht gespeichert (Outlook-Zusatzreferenz) wurde](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Gibt an, ob das Bild eines Kontakts in Outlook (Outlook-Zusatzreferenz) anzeigen](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
- [Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)](available-events-and-their-dispids-outlook-exported-apis.md)

