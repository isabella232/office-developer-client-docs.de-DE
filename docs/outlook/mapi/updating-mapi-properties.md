---
title: Aktualisieren von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 172abe64073b11d98bfb5f76999237218ef8944a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581349"
---
# <a name="updating-mapi-properties"></a>Aktualisieren von MAPI-Eigenschaften

**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

