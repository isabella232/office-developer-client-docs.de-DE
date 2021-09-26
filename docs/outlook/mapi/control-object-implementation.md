---
title: Implementierung von Steuerelementobjekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5484aeca5b09578fbfb6dd4758217b98cba9ac67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611026"
---
# <a name="control-object-implementation"></a>Implementierung von Steuerelementobjekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Steuerelementobjekte oder Objekte, die die [IMAPIControl : IUnknown-Schnittstelle](imapicontroliunknown.md) unterstützen, werden von Anbietern implementiert, um einer Schaltfläche, die in einem MAPI-Dialogfeld angezeigt wird, Funktionen hinzuzufügen. Steuerelementobjekte können nur für Schaltflächen implementiert werden. 
  
 **IMAPIControl** verfügt über drei Methoden: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)und [Activate](imapicontrol-activate.md). 
  
MAPI ruft **GetState** auf, um zu bestimmen, ob die Schaltfläche deaktiviert werden soll. **GetState** wird in den folgenden Situationen aufgerufen: 
  
- Wenn das Dialogfeld, in dem die Schaltfläche angezeigt wird, zum ersten Mal angezeigt wird.
    
- Wenn eine Anzeigetabellenbenachrichtigung für die Schaltfläche ausgegeben wird. 
    
Legen Sie den Inhalt des  _lpulState-Parameters_ auf MAPI_DISABLED fest, wenn der Benutzer nicht mit der Schaltfläche interagieren kann, und MAPI_ENABLED, ob der Benutzer interagieren kann. 
  
Wenn der Benutzer auf die Schaltfläche klickt, ruft MAPI **activate** auf. **Activate** führt die Aufgabe aus, die der Schaltfläche zugeordnet wurde. Diese Aufgabe kann für Ihren Anbieter geeignet sein, z. B. das Anzeigen eines Dialogfelds oder das Aktualisieren einer Eigenschaft. Wenn die Aufgabe nicht erfolgreich ist, weil der Benutzer sie abgebrochen hat, geben Sie MAPI_E_USER_CANCEL zurück. Geben Sie für andere Fehlerursachen den entsprechenden Fehlerwert zurück. 
  
Wenn die Aufgabe erfolgreich ist und mit einer Eigenschaftsänderung verknüpft ist, die in einem anderen Steuerelement des Dialogfelds widergespiegelt wird, rufen Sie [ITableData::HrNotify](itabledata-hrnotify.md)auf. **HrNotify** wird aufgerufen, um eine Anzeigetabellenbenachrichtigung mit der **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) -Eigenschaft der geänderten Eigenschaft in der [TABLE_NOTIFICATION](table_notification.md) Struktur auszugeben. Platzieren Sie den neuen Eigenschaftswert nicht in der Struktur. geben Sie sie stattdessen zurück, wenn [IMAPIProp::GetProps](imapiprop-getprops.md) aufgerufen wird. Obwohl in der Regel eine Anzeigetabellenbenachrichtigung nicht zum Deaktivieren oder Aktivieren eines Steuerelements verwendet werden kann, kann sie mit einer Schaltfläche verwendet werden. MAPI aktualisiert das geänderte Steuerelement, um auf die Benachrichtigung zu reagieren. 
  
MAPI ruft die **GetLastError-Methode** des Steuerelements auf, wenn **Activate** einen anderen Fehler als MAPI_E_USER_CANCEL zurückgibt. If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

