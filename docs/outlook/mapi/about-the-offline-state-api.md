---
title: Informationen zur Offlinestatus-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 520ee2b76c851cfdb112f7be72fcb48ea9f38c01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614325"
---
# <a name="about-the-offline-state-api"></a>Informationen zur Offlinestatus-API

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Offlinestatus-API unterstützt Rückrufe, die Änderungen im Verbindungsstatus eines Benutzers in Microsoft Outlook 2013 und Microsoft Outlook 2010 angeben, z. B. von der Online-Nutzung in Outlook 2013 oder Outlook 2010 bis zum Offlinemodus. Die API verwendet ein globales Offlineobjekt in Outlook 2013 oder Outlook 2010, um solche Änderungen für ein bestimmtes Benutzerkontoprofil nachzuverfolgen. Benachrichtigung ist die einzige unterstützte Form des Rückrufs. Als Clients dieser API führen E-Mail-Anbieter, die über solche Verbindungsstatusänderungen benachrichtigt werden möchten, folgende Aktionen aus:
  
1. Implementieren Sie **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Öffnen Sie ein vorhandenes Offlineobjekt für ein bestimmtes Profil mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Ermitteln Sie, ob das Objekt online oder offline Benachrichtigungen mit **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** bereitstellen kann. 
    
4. Registrieren Sie das Objekt für Online- oder Offlinebenachrichtigungen mit **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. E-Mail-Anbieter können jetzt Benachrichtigungen empfangen, die Outlook 2013 oder Outlook 2010 mit **IMAPIOfflineNotify** senden. 
    
5. Entfernen Sie beim Herunterfahren die Registrierung für Online- und Offlinebenachrichtigungen mit **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> Im Allgemeinen können Outlook 2013 und Outlook 2010 einen Client über Online-/Offlineänderungen sowie andere Änderungen benachrichtigen, aber die Offlinestatus-API unterstützt nur Benachrichtigungen für Online-/Offlineänderungen. Der Client sollte alle anderen Benachrichtigungen ignorieren. Weitere Informationen finden Sie unter **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Ein Beispiel für einen Client, der die Offlinestatus-API verwendet, finden Sie unter ["Informationen zum Offlinestatus-Beispiel-Add-In".](about-the-sample-offline-state-add-in.md) Das Offlinestatus-Beispiel-Add-In ist ein COM-Add-In, das die Offlinestatus-API verwendet, um den Verbindungsstatus zu überwachen und zu ändern.
  
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
    

