---
title: Implementierung der Steuerelement-Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 268ad60cf8161fb2b58370f89aae623aabd7da7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791449"
---
# <a name="control-object-implementation"></a>Implementierung der Steuerelement-Objekts

  
  
**Betrifft**: Outlook 
  
Steuerelement-Objekte oder Objekte, die unterstützen die [IMAPIControl: IUnknown](imapicontroliunknown.md) Schnittstelle, die implementiert werden, von Anbietern Funktionen eine Schaltfläche hinzu, die in einem MAPI-Dialogfeld angezeigt wird. Control-Objekte können nur für Schaltflächen implementiert werden. 
  
 **IMAPIControl** verfügt über drei Methoden: [GetLastError](imapicontrol-getlasterror.md) [GetState](imapicontrol-getstate.md)und zu [Aktivieren](imapicontrol-activate.md). 
  
MAPI-Aufrufen **GetState** , um zu bestimmen, ob die Schaltfläche zu deaktivieren. **GetState** wird in den folgenden Situationen aufgerufen: 
  
- Wenn das Dialogfeld, in dem die Schaltfläche angezeigt wird, zuerst angezeigt wird.
    
- Wenn eine Anzeige Tabelle Benachrichtigung für die Schaltfläche ausgestellt wurde. 
    
Legen Sie den Inhalt des Parameters _LpulState_ auf MAPI_DISABLED, wenn der Benutzer mit der Schaltfläche und MAPI_ENABLED interagieren kann, wenn der Benutzer interagieren kann. 
  
Wenn der Benutzer auf die Schaltfläche klickt, ruft MAPI **Aktivieren**. **Activate** führt die Aufgabe, die die Schaltfläche zugeordnet wurde. Für diese Aufgabe kann beliebig für Ihren Anbieter, wie ein Dialogfeld angezeigt, oder Aktualisieren einer Eigenschaft geeignet sein. Wenn der Vorgang nicht erfolgreich ist, da der Benutzer den Vorgang abgebrochen, geben Sie MAPI_E_USER_CANCEL zurück. Weitere Ursachen des Fehlers den entsprechenden Fehlerwert zurück. 
  
Rufen Sie [ITableData::HrNotify](itabledata-hrnotify.md), wenn der Vorgang erfolgreich ist und mit einer Änderung der Eigenschaft, die in ein anderes Steuerelement im Dialogfeld wiedergegeben wird verknüpft ist. **HrNotify** wird aufgerufen, um eine Anzeige Tabelle Benachrichtigung mit der geänderten **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))-Eigenschaft in der Struktur [TABLE_NOTIFICATION](table_notification.md) Problem. Setzen Sie den neuen Eigenschaftswert nicht in der Struktur. Stattdessen geben sie zurück, wenn [IMAPIProp::GetProps](imapiprop-getprops.md) aufgerufen wird. Zwar in der Regel eine Anzeige-Tabelle-Benachrichtigung nicht zum Deaktivieren oder Aktivieren eines Steuerelements, können sie mit einer Schaltfläche verwendet werden. MAPI wird das geänderte Steuerelement, um auf die Benachrichtigung reagieren aktualisiert. 
  
MAPI-Aufrufen **GetLastError** -Methode des Steuerelements, wenn **Activate** als MAPI_E_USER_CANCEL einen Fehler zurückgegeben. Wenn **GetLastError** erweiterte Fehlerinformationen in der Struktur [MAPIERROR](mapierror.md) , die sie in den Inhalt des Parameters _LppMAPIError_ zurückgibt tätigt, von MAPI für den Benutzer angezeigt. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

