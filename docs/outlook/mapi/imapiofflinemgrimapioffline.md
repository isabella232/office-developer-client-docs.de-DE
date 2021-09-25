---
title: IMAPIOfflineMgr IMAPIOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineMgr
api_type:
- COM
ms.assetid: 3e430308-190c-c9bb-fffc-c26ffecb73a5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0b61a4017ee8763e07647b1f4c3eca6fef7d4fe2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630691"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt die Registrierung für Benachrichtigungsrückrufe zu Verbindungsstatusänderungen eines Benutzerkontos.
  
|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32.dll  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Beraten](imapiofflinemgr-advise.md) <br/> |Registriert Benachrichtigungsrückrufe zu Verbindungsänderungen.  <br/> |
|[Unadvise](imapiofflinemgr-unadvise.md) <br/> |Entfernt eine bestimmte Registrierung für Benachrichtigungsrückrufe.  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Beim Öffnen eines Offlineobjekts für ein Benutzerkontoprofil mit **[HrOpenOfflineObj](hropenofflineobj.md)** ruft ein Client ein Offlineobjekt ab, das **IMAPIOfflineMgr** unterstützt. 
  
Da diese Schnittstelle von **[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)** erbt, kann der Client diese Schnittstelle (mithilfe von **[IUnknown::QueryInterface)](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** abfragen, um ein Objekt abzurufen, das **[IMAPIOffline](imapiofflineiunknown.md)** unterstützt. Der Client kann sich dann über die Rückruffunktionen des Offlineobjekts (durch Aufrufen von **[IMAPIOffline::GetCapabilities)](imapioffline-getcapabilities.md)** informieren und sich für die Einrichtung von Rückrufen entscheiden (mithilfe von **IMAPIOfflineMgr::Advise** ). 
  
Die meisten Elemente in dieser Schnittstelle sind Platzhalter, die für die interne Verwendung von Outlook reserviert sind und änderungen vorbehalten sind. Aufrufer dieser Schnittstelle dürfen Elemente, die keine Platzhalter sind, nur als dokumentiert verwenden.
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[MAPI-Schnittstellen](mapi-interfaces.md)

