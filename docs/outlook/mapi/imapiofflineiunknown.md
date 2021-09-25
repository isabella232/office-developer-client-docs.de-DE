---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4531b7e4b2d1e88c994bd548721d1a4a88db050b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630705"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Informationen für ein Offlineobjekt bereit.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Abfrage [für IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Legt den aktuellen Status eines Offlineobjekts auf "Online" oder "Offline" fest.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Ruft die Bedingungen ab, unter denen Rückrufe von einem Offlineobjekt unterstützt werden.  <br/> |
|**[Getcurrentstate](imapioffline-getcurrentstate.md)** <br/> |Ruft den aktuellen Online- oder Offlinestatus eines Offlineobjekts ab.  <br/> |
| *Platzhalterelement*  <br/> |Dieser Member ist ein Platzhalter und wird nicht unterstützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Client verwendet **[HrOpenOfflineObj](hropenofflineobj.md)** zum Öffnen und Abrufen eines Offlineobjekts, das **IMAPIOfflineMgr** unterstützt. Da **IMAPIOfflineMgr** von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)erbt, kann der Client diese Schnittstelle (mithilfe von [IUnknown::QueryInterface)](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)abfragen, um einen Zeiger auf den Schnittstellenzeiger für **IMAPIOffline** für das Offlineobjekt abzurufen. Der Client kann dann den aktuellen Status des Objekts abrufen oder festlegen oder sich über die Rückruffunktionen des Objekts (durch Aufrufen von **IMAPIOffline::GetCapabilities)** informieren und rückrufe mithilfe von **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** einrichten. 
  
Ein Mitglied in dieser Schnittstelle ist ein Platzhalter, der für die interne Verwendung von Microsoft Outlook 2013 reserviert ist, und kann geändert werden. Andere Elemente in dieser Schnittstelle dürfen nur als dokumentiert verwendet werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[MAPI-Schnittstellen](mapi-interfaces.md)

