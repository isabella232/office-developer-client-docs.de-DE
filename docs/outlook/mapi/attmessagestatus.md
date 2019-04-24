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
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318214"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Nachrichtenkennzeichen werden TNEF-Flags zugeordnet, um die Abwärtskompatibilität beizubehalten. Alle Flags werden zusammengefasst und in einem einzigen Byte codiert. Die Zuordnungen lauten wie folgt:
  
|**MAPI-Nachrichtenkennzeichen**|**TNEF-Flags**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Diese Flags werden im TNEF definiert. H-Headerdatei.
  

