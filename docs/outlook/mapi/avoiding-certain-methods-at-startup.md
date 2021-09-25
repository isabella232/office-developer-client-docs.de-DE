---
title: Vermeiden bestimmter Methoden beim Start
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Zuletzt geändert: 07. Dezember 2015'
ms.openlocfilehash: 345633700d921f617f65e0b5fefeba05deba7c72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605139"
---
# <a name="avoiding-certain-methods-at-startup"></a>Vermeiden bestimmter Methoden beim Start

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zur Verbesserung der Leistung beim Starte vermeiden Sie die folgenden Aufrufe:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
Der Aufruf von **IMAPIStatus::ValidateState** wirkt sich nur dann auf die Leistung aus, wenn er entweder im MAPI-Spooler oder im MAPI-Untersystem vorgenommen wird. Der Grund dafür, warum diese Methoden den Systemstartvorgang verlangsamen, liegt darin, dass sie erst abgeschlossen werden können, wenn der MAPI-Spooler seine Startaufgaben abgeschlossen hat. 
  
Sie sollten beim Systemstart auch nicht den Nachrichtenspeicher durchsuchen. Tätigen Sie den [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)-Aufruf, wenn der Startvorgang abgeschlossen ist. 
  

