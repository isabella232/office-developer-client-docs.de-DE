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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 616bb4774e2ca5385e7da867477cb8849d94336b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568385"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen für eine offline-Objekt.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |Abfrage für [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Legt den aktuellen Zustand eines offline-Objekts zu online oder offline.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Ruft die Bedingungen für die Rückrufe durch eine offline-Objekt unterstützt werden.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Ruft den aktuellen online oder offline-Status eines offline-Objekts ab.  <br/> |
| *Platzhalter-member*  <br/> |Dieser Member ist ein Platzhalter und wird nicht unterstützt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein Client verwendet **[HrOpenOfflineObj](hropenofflineobj.md)** zu öffnen, und erhalten eine offline-Objekt, das **IMAPIOfflineMgr**unterstützt. Da **IMAPIOfflineMgr** von [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)erbt, kann der Client (mithilfe von [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)) diese Schnittstelle Abfragen um einen Zeiger auf den Zeiger der Schnittstelle für **IMAPIOffline** für das offline-Objekt abzurufen. Der Client kann dann abzurufen oder festzulegen den aktuellen Status des Objekts zugreifen, oder informieren Sie sich über die Callback-Funktionen des Objekts (durch Aufrufen von **IMAPIOffline::GetCapabilities** ) und auf Rückrufe mithilfe von **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** eingerichtet werden sollen. 
  
Ein Element in dieser Schnittstelle ist ein Platzhalter für die interne Verwendung von Microsoft Outlook 2013 reserviert und kann geändert werden. Andere Member in dieser Schnittstelle müssen nur gemäß Dokumentation verwendet werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Informationen zu der Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[MAPI-Schnittstellen](mapi-interfaces.md)

