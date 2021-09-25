---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 094067ef80175cf2d87ccea24239be3eadb70774
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564176"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt Microsoft Outlook 2010 und Microsoft Outlook 2013 beim Senden von Benachrichtigungsrückrufen an einen Client.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Notify](imapiofflinenotify-notify.md) <br/> |Sendet Benachrichtigungen zu Änderungen im Verbindungsstatus an einen Client.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Client muss diese Schnittstelle implementieren und einen Zeiger als Mitglied in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** übergeben, wenn Callbacks mit **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** eingerichtet werden. Anschließend können Outlook 2010 oder Outlook 2013 diese Schnittstelle verwenden, um Benachrichtigungsrückrufe an den Client zu senden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

