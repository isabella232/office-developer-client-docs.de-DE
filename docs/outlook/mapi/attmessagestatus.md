---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ce34b9b3b3c2f8a3a3f6814507225145eb39d86b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564434"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Nachrichtenflags werden TNEF-Flags zugeordnet, um die Abwärtskompatibilität zu erhalten. Alle Flags werden gruppiert und in einem einzigen Byte codiert. Die Zuordnungen sind wie folgt:
  
|**MAPI-Nachrichtenflags**|**TNEF-Flags**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Diese Flags sind im TNEF definiert. H-Headerdatei.
  

