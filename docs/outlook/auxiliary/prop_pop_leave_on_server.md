---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Gibt an, dass eine Kopie einer Nachricht für ein POP-Konto auf dem Server verbleibt.
ms.openlocfilehash: 34626447e92f9bce2d1dbf32451e46414286c1bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605279"
---
# <a name="prop_pop_leave_on_server"></a>PROP_POP_LEAVE_ON_SERVER

Gibt an, dass eine Kopie einer Nachricht für ein POP-Konto auf dem Server verbleibt.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Kennung:  <br/> |0x1000  <br/> |
|Eigenschaftentyp:  <br/> |PT_DWORD  <br/> |
|Eigenschaftstag:  <br/> |0x10000003  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In der folgenden Tabelle sind die möglichen Werte aufgeführt. Weitere Informationen zu den Konstanten finden Sie unter [Konstanten (Kontoverwaltungs-API).](constants-account-management-api.md) 
  
|**Mögliche Werte**|**Beschreibung**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Hinterlässt eine Kopie der Nachricht auf dem POP-Server, nachdem die Nachricht auf ein Gerät heruntergeladen wurde.  <br/> |
|**REMOVE_AFTER** <br/> |Entfernt die Nachricht vom POP-Server, nachdem sie auf ein Gerät heruntergeladen wurde.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Entfernt die Nachricht erst vom POP-Server, nachdem der Benutzer die Nachricht aus dem Ordner "Gelöschte Elemente" gelöscht hat.  <br/> |
|**GET_REMOVE_AFTER_DAYS**( _ul_)  <br/> |Ruft die Anzahl der Tage ab, nach denen die Nachricht vom POP-Server entfernt wird.  <br/> |
|**SET_REMOVE_AFTER_DAYS**( _Tage_)  <br/> |Legt die Anzahl der Tage fest, nach denen die Nachricht vom POP-Server entfernt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

