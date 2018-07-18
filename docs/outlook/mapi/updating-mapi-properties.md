---
title: Aktualisieren von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5cff3a6cbf4bfca7b414f9663e71834da71926d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795785"
---
# <a name="updating-mapi-properties"></a>Aktualisieren von MAPI-Eigenschaften

**Betrifft**: Outlook 
  
Clients und Dienstanbieter können durch Aufrufen ein Eigenschaftswerts aktualisieren:
  
- Ein Objekt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode zum Aktualisieren des Werts, der eine oder mehrere der Eigenschaften eines Objekts. 
    
- Die [HrSetOneProp](hrsetoneprop.md) -Funktion, die nur eine Eigenschaft gleichzeitig zu aktualisieren. Verwenden Sie **HrSetOneProp** , nur, wenn das Zielobjekt lokalen ist. Diese Funktion kann zu Leistungseinbußen bei der remote-Objekte mit führen. 
    
Das folgende Verfahren veranschaulicht, wie **SetProps** verwenden, um die Nachrichtenklasse, oder die Eigenschaft PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) einer Nachricht zu aktualisieren. 
  
### <a name="to-update-the-message-class-of-a-message"></a>So aktualisieren Sie die Nachrichtenklasse einer Nachricht 
  
1. Reservieren Sie eine [SPropValue](spropvalue.md) -Struktur für die Nachrichtenklasse und festlegen Sie seine Member entsprechend. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Rufen Sie die Nachricht **IMAPIProp::SetProps** -Methode, um die neue Nachrichtenklasse festzulegen. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

