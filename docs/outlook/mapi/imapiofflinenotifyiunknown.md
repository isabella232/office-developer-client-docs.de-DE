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
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568147"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Senden von Benachrichtigungen Rückrufe an einen Client unterstützt Microsoft Outlook 2010 und Microsoft Outlook 2013.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Benachrichtigen](imapiofflinenotify-notify.md) <br/> |Sendet Benachrichtigungen an einen Client zu Änderungen in Verbindungsstatus.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Client muss diese Schnittstelle implementieren und einen Zeiger darauf als Mitglied in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** übergeben, beim Einrichten von Rückrufe mit **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Anschließend werden Outlook 2010 oder Outlook 2013 können diese Schnittstelle verwenden, um die Benachrichtigung Rückrufe an den Client gesendet. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Informationen zu der Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

