---
title: Implementierung des Steuerelementobjekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422607"
---
# <a name="control-object-implementation"></a>Implementierung des Steuerelementobjekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Steuerelementobjekte oder Objekte, die die [IMAPIControl : IUnknown-Schnittstelle](imapicontroliunknown.md) unterstützen, werden von Anbietern implementiert, um einer Schaltfläche, die in einem MAPI-Dialogfeld angezeigt wird, Funktionalität hinzuzufügen. Steuerelementobjekte können nur für Schaltflächen implementiert werden. 
  
 **IMAPIControl** verfügt über drei Methoden: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)und [Activate](imapicontrol-activate.md). 
  
MAPI ruft **GetState auf,** um zu bestimmen, ob die Schaltfläche deaktiviert werden soll. **GetState** wird in den folgenden Situationen aufgerufen: 
  
- Wenn das Dialogfeld, in dem die Schaltfläche angezeigt wird, zum ersten Mal angezeigt wird.
    
- Wenn eine Anzeigetabelle für die Schaltfläche ausgegeben wird. 
    
Legen Sie den Inhalt des  _lpulState-Parameters_ auf MAPI_DISABLED, wenn der Benutzer nicht mit der Schaltfläche interagieren kann, und MAPI_ENABLED, wenn der Benutzer interagieren kann. 
  
Wenn der Benutzer auf die Schaltfläche klickt, ruft MAPI **Activate auf.** **Activate** führt die Aufgabe aus, die der Schaltfläche zugeordnet wurde. Diese Aufgabe kann für Ihren Anbieter geeignet sein, z. B. das Anzeigen eines Dialogfelds oder das Aktualisieren einer Eigenschaft. Wenn die Aufgabe nicht erfolgreich war, weil der Benutzer sie abgebrochen hat, geben Sie MAPI_E_USER_CANCEL. Geben Sie bei anderen Fehlerursachen den entsprechenden Fehlerwert zurück. 
  
Wenn der Vorgang erfolgreich ist und mit einer Eigenschaftsänderung verknüpft ist, die in einem anderen Steuerelement im Dialogfeld widerspiegelt wird, rufen Sie [ITableData::HrNotify auf.](itabledata-hrnotify.md) **HrNotify** wird aufgerufen, um eine Anzeigetabelle mit der **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) -Eigenschaft der geänderten Eigenschaft in der TABLE_NOTIFICATION [aus.](table_notification.md) Platzieren Sie den neuen Eigenschaftswert nicht in der Struktur. geben Sie es stattdessen zurück, wenn [IMAPIProp::GetProps](imapiprop-getprops.md) aufgerufen wird. Obwohl in der Regel keine Anzeigetabelle zum Deaktivieren oder Aktivieren eines Steuerelements verwendet werden kann, kann sie mit einer Schaltfläche verwendet werden. MAPI aktualisiert das geänderte Steuerelement, um auf die Benachrichtigung zu reagieren. 
  
MAPI ruft die **GetLastError-Methode** des Steuerelements auf, wenn **Activate** einen anderen Fehler als MAPI_E_USER_CANCEL. Wenn **GetLastError** erweiterte Fehlerinformationen in der [MAPIERROR-Struktur](mapierror.md) platziert, die im Inhalt des  _lppMAPIError-Parameters_ zurückgegeben wird, zeigt MAPI sie für den Benutzer an. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

