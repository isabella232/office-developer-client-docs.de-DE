---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791344"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Betrifft**: Outlook 
  
TNEF-Flags Abwärtskompatibilität beibehalten werden MAPI Nachrichtenflags zugeordnet. Alle Flags werden zusammengefasst und in ein einzelnes Byte codiert. Die Zuordnungen lauten wie folgt:
  
|**MAPI-Nachrichtenflags**|**TNEF-Kennzeichen**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ FmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Diese Flags werden in die TNEF definiert. H-Headerdatei.
  

