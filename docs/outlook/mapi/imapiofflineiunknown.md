---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321266"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Informationen für ein Offlineobjekt bereit.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Abfrage auf [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Legt den aktuellen Status eines Offline Objekts auf Online oder offline fest.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Ruft die Bedingungen ab, für die Rückrufe von einem Offlineobjekt unterstützt werden.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Ruft den aktuellen Online-oder Offlinestatus eines Offline Objekts ab.  <br/> |
| *Platzhalterelement*  <br/> |Dieser Member ist ein Platzhalter und wird nicht unterstützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Client verwendet **[HrOpenOfflineObj](hropenofflineobj.md)** zum Öffnen und Abrufen eines Offline Objekts, das **IMAPIOfflineMgr**unterstützt. Da **IMAPIOfflineMgr** von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)erbt, kann der Client diese Schnittstelle Abfragen (mithilfe von [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)), um einen Zeiger auf den Schnittstellenzeiger für **IMAPIOffline** für das Offlineobjekt abzurufen. Der Client kann dann den aktuellen Status des Objekts abrufen oder festlegen oder sich über die Rückruffunktionen des Objekts informieren (durch Aufrufen von **IMAPIOffline:: getCapabilities** ) und das Einrichten von Rückrufen mithilfe von **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. 
  
Ein Mitglied dieser Schnittstelle ist ein Platzhalter für die interne Verwendung von Microsoft Outlook 2013 und kann geändert werden. Andere Elemente in dieser Schnittstelle dürfen nur wie dokumentiert verwendet werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[MAPI-Schnittstellen](mapi-interfaces.md)

