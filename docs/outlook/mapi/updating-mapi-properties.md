---
title: Aktualisieren von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 90af0f7226acbdbab4fde6480763d3415236cfcc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623971"
---
# <a name="updating-mapi-properties"></a>Aktualisieren von MAPI-Eigenschaften

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients und Dienstanbieter können einen Eigenschaftswert aktualisieren, indem sie Folgendes aufrufen:
  
- Die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) eines Objekts zum Aktualisieren des Werts einer oder mehrerer Eigenschaften eines Objekts. 
    
- Die [HrSetOneProp-Funktion,](hrsetoneprop.md) um jeweils nur eine Eigenschaft zu aktualisieren. Verwenden Sie **HrSetOneProp** nur, wenn das Zielobjekt lokal ist. Diese Funktion kann bei Verwendung mit Remoteobjekten zu leistungsbeeinträchtigungen führen. 
    
Das folgende Verfahren veranschaulicht die Verwendung von **SetProps** zum Aktualisieren der Nachrichtenklasse oder PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft einer Nachricht. 
  
### <a name="to-update-the-message-class-of-a-message"></a>So aktualisieren Sie die Nachrichtenklasse einer Nachricht 
  
1. Weisen Sie der Nachrichtenklasse eine [SPropValue-Struktur](spropvalue.md) zu, und legen Sie deren Member entsprechend fest. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Rufen Sie die **IMAPIProp::SetProps-Methode** der Nachricht auf, um die neue Nachrichtenklasse festzulegen. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

