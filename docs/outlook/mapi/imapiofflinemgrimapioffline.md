---
title: IMAPIOfflineMgr IMAPIOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr
api_type:
- COM
ms.assetid: 3e430308-190c-c9bb-fffc-c26ffecb73a5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 235c2afb20e6f36df72eac4070c1df5fd10fcce8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270091"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt die Registrierung von Benachrichtigungs Rückrufen über Verbindungsstatusänderungen eines Benutzerkontos.
  
|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32. dll  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Beraten](imapiofflinemgr-advise.md) <br/> |Register für Benachrichtigungsrückrufe zu Verbindungsänderungen.  <br/> |
|[Unadvise](imapiofflinemgr-unadvise.md) <br/> |Entfernt eine bestimmte Registrierung für Benachrichtigungsrückrufe.  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
| *Platzhalterelement*  <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Beim Öffnen eines Offline Objekts für ein Benutzerkontoprofil mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)** Ruft ein Client ein Offlineobjekt ab, das **IMAPIOfflineMgr**unterstützt. 
  
Da diese Schnittstelle von **[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)** erbt, kann der Client diese Schnittstelle Abfragen (mithilfe von **[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** ), um ein Objekt abzurufen, das **[IMAPIOffline](imapiofflineiunknown.md)** unterstützt. Der Client kann sich dann über die Rückruffunktionen des Offline Objekts informieren (durch Aufrufen von **[IMAPIOffline:: getCapabilities](imapioffline-getcapabilities.md)** ) und das Einrichten von Rückrufen (mithilfe von **IMAPIOfflineMgr:: Advise** ). 
  
Bei den meisten Mitgliedern dieser Schnittstelle handelt es sich um Platzhalter, die für die interne Verwendung von Outlook reserviert sind und Änderungen unterliegen. Aufrufer dieser Schnittstelle dürfen nicht-Platzhalterelemente nur wie dokumentiert verwenden.
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[MAPI-Schnittstellen](mapi-interfaces.md)

