---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439877"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt Microsoft Outlook 2010 und Microsoft Outlook 2013 beim Senden von Benachrichtigungsrückrufen an einen Client.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Notify](imapiofflinenotify-notify.md) <br/> |Sendet Benachrichtigungen über Änderungen im Verbindungsstatus an einen Client.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Client muss diese Schnittstelle implementieren und einen Zeiger als Mitglied **[in](mapioffline_adviseinfo.md)** MAPIOFFLINE_ADVISEINFO beim Einrichten von Rückrufen mit **[IMAPIOfflineMgr::Advise übergeben.](imapiofflinemgr-advise.md)** Anschließend können Outlook 2010 oder Outlook 2013 diese Schnittstelle verwenden, um Benachrichtigungsrückrufe an den Client zu senden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

