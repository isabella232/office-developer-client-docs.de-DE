---
title: Informationen zur Offlinestatus-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321791"
---
# <a name="about-the-offline-state-api"></a>Informationen zur Offlinestatus-API

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Offlinestatus-API unterstützt Rückrufe, die Änderungen des Verbindungsstatus eines Benutzers in Microsoft Outlook 2013 und Microsoft Outlook 2010 angeben, beispielsweise von der Online Funktion in Outlook 2013 oder Outlook 2010 zum Offline schalten. Die API verwendet ein globales Offline-Objekt in Outlook 2013 oder Outlook 2010, um solche Änderungen für ein bestimmtes Benutzerkontoprofil nachzuverfolgen. Benachrichtigung ist das einzige unterstützte Rückrufformular. Als Clients dieser API gehen e-Mail-Anbieter, die über einen solchen Verbindungsstatus benachrichtigt werden möchten, wie folgt vor:
  
1. Implementieren Sie **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Öffnen Sie ein vorhandenes Offline-Objekt für ein bestimmtes Profil mit **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Bestimmen Sie, ob das Objekt über die Möglichkeit zum Bereitstellen von Online-oder offline Benachrichtigungen mithilfe von **[IMAPIOffline:: getCapabilities](imapioffline-getcapabilities.md)** verfügt. 
    
4. Registrieren Sie das Objekt für Online-oder offline Benachrichtigungen mit **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**. E-Mail-Anbieter können jetzt Benachrichtigungen erhalten, die von Outlook 2013 oder Outlook 2010 mithilfe von **IMAPIOfflineNotify**gesendet werden. 
    
5. Entfernen Sie beim Herunterfahren die Registrierung für Online-und Offline Benachrichtigungen mit **[IMAPIOfflineMgr:: Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> Im Allgemeinen können Outlook 2013 und Outlook 2010 einen Client über Online-/Offline-Änderungen sowie andere Änderungen informieren, die Offlinestatus-API unterstützt jedoch nur Benachrichtigungen für Online/Offline-Änderungen. Der Client sollte alle anderen Benachrichtigungen ignorieren. Weitere Informationen finden Sie unter **[IMAPIOfflineNotify:: notify](imapiofflinenotify-notify.md)** und **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Ein Beispiel für einen Client, der die Offlinestatus-API verwendet, finden Sie unter [Informationen zum Offlinestatus-Add-in-Beispiel](about-the-sample-offline-state-add-in.md). Das Beispiel für Offlinestatus-Add-in ist ein COM-Add-in, das die Offline Status-API verwendet, um den Verbindungsstatus zu überwachen und zu ändern.
  
Diese API bietet Folgendes:
  
Definitionen:
  
- [MAPI-Konstanten](mapi-constants.md)
    
Datentypen:
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
Funktionen:
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
Schnittstellen:
  
- **[IMAPIOffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    

