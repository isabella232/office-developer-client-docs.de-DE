---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Gibt an, wobei eine Kopie einer Nachricht auf dem Server für ein POP-Konto.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791193"
---
# <a name="proppopleaveonserver"></a>PROP_POP_LEAVE_ON_SERVER

Gibt an, wobei eine Kopie einer Nachricht auf dem Server für ein POP-Konto.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Bezeichner:  <br/> |0 x 1000  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_DWORD  <br/> |
|Eigenschafts-Tag:  <br/> |0x10000003  <br/> |
|Access:  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Hinweise

In der folgenden Tabelle sind die möglichen Werte aufgeführt. Weitere Informationen zu Konstanten finden Sie unter [Konstanten (Konto Management-API)](constants-account-management-api.md) . 
  
|**Mögliche Werte**|**Beschreibung**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Bewirkt, dass eine Kopie der Nachricht auf dem POP-Server nach dem Herunterladen der Nachricht zu einem Gerät.  <br/> |
|**REMOVE_AFTER** <br/> |Entfernt die Nachricht vom POP-Server nach dem Herunterladen zu einem Gerät.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Entfernt die Nachricht vom POP-Server, nur, nachdem der Benutzer die Nachricht aus dem Ordner Gelöschte Elemente löscht.  <br/> |
|**GET_REMOVE_AFTER_DAYS** ( _Ul_)  <br/> |Ruft die Anzahl der Tage nach denen die Nachricht vom POP-Server entfernt wird.  <br/> |
|**SET_REMOVE_AFTER_DAYS** ( _Tage_)  <br/> |Legt die Anzahl der Tage nach denen die Nachricht vom POP-Server entfernt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Verwalten von Nachricht downloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)

