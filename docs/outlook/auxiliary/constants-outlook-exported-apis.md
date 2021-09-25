---
title: Konstanten (Outlook exportierter APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Dieses Thema enthält Konstantendefinitionen für APIs, die Exporte Outlook.
ms.openlocfilehash: 0ba6c94ad8f4e5ed78d8f6b4e2ea56ba8258c4e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614465"
---
# <a name="constants-outlook-exported-apis"></a>Konstanten (Outlook exportierter APIs)

Dieses Thema enthält Konstantendefinitionen für APIs, die Exporte Outlook.
  
## <a name="definitions-for-time-zone-support"></a>Definitionen für die Zeitzonenunterstützung

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Definitionen für die Kategorieunterstützung

|**Konstante**|**Definition**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Verschiedene Verteiler-IDs

Outlook macht die folgenden Verteiler-IDs (Dispids) verfügbar, sodass Entwickler [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) verwenden können, um auf die entsprechende Eigenschaft oder Methode zuzugreifen oder das entsprechende Ereignis abzuhören. 
  
|**Zugeordnete Konstante**|**Dispid-Wert**|**Beschreibung**|**Anwendbare Schnittstelle**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Wird verwendet, um die entsprechende Eigenschaft für ein Element aufzurufen, um zu überprüfen, ob das Element geändert, aber nicht gespeichert wurde.  <br/> |Objekte auf Elementebene  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Wird verwendet, um die entsprechende Methode im Explorer oder Inspektor aufzurufen, um anzugeben, ob das Bild eines Kontakts basierend auf einem bestimmten Argument angezeigt werden soll.  <br/> |Explorer oder Inspektor  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Wird verwendet, um das Ereignis aus der **IDispatch::Invoke-Funktion** zu behandeln, die vor einem Druckvorgang ausgelöst wird.  <br/> |Application  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Wird verwendet, um das Ereignis aus der **IDispatch::Invoke-Funktion** zu behandeln, die ausgelöst wird, wenn Outlook das Lesen der Eigenschaften des Elements abgeschlossen hat.  <br/> |Objekte auf Elementebene  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Aus Outlook exportierte APIs](outlook-exported-apis.md)
- [Informationen zu von Outlook exportierten APIs](about-apis-exported-by-outlook.md)
- [Bestimmen Sie, ob ein Outlook-Element geändert, aber nicht gespeichert (Outlook 2013 Hilfs-Referenz) wurde](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Geben Sie an, ob das Bild eines Kontakts in Outlook (Outlook-Zusatzreferenz) angezeigt werden soll](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)](available-events-and-their-dispids-outlook-exported-apis.md)

