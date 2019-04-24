---
title: Implementierung des Control-Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335658"
---
# <a name="control-object-implementation"></a>Implementierung des Control-Objekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Steuerelementobjekte oder Objekte, die die [IMAPIControl: IUnknown](imapicontroliunknown.md) -Schnittstelle unterstützen, werden von Anbietern implementiert, um einer Schaltfläche, die in einem MAPI-Dialogfeld angezeigt wird, Funktionalität hinzuzufügen. Steuerelemente können nur für Schaltflächen implementiert werden. 
  
 **IMAPIControl** verfügt über drei Methoden: [Getlasterroraufzurufen](imapicontrol-getlasterror.md), GetState und [Activate](imapicontrol-activate.md). [](imapicontrol-getstate.md) 
  
MAPI ruft **GetState** auf, um zu bestimmen, ob die Schaltfläche deaktiviert werden soll. **GetState** wird in den folgenden Situationen aufgerufen: 
  
- Wenn das Dialogfeld, in dem die Schaltfläche angezeigt wird, zuerst angezeigt wird.
    
- Wenn eine Anzeige Tabellenbenachrichtigung für die Schaltfläche ausgegeben wird. 
    
Legen Sie den Inhalt des _lpulState_ -Parameters auf MAPI_DISABLED fest, wenn der Benutzer nicht mit der Schaltfläche und MAPI_ENABLED interagieren kann, wenn der Benutzer interagieren darf. 
  
Wenn der Benutzer auf die Schaltfläche klickt, ruft MAPI die **Aktivierung**auf. **Activate** führt die Aufgabe aus, die der Schaltfläche zugeordnet wurde. Diese Aufgabe kann für Ihren Anbieter geeignet sein, wie beispielsweise Anzeigen eines Dialogfelds oder Aktualisieren einer Eigenschaft. Wenn die Aufgabe nicht erfolgreich ist, weil der Benutzer sie abgebrochen hat, geben Sie MAPI_E_USER_CANCEL zurück. Geben Sie für weitere Fehlerursachen den entsprechenden Fehlerwert zurück. 
  
Wenn die Aufgabe erfolgreich ist und mit einer Eigenschaftenänderung verknüpft ist, die in einem anderen Steuerelement des Dialogfelds angezeigt wird, rufen Sie [ITableData:: HrNotify](itabledata-hrnotify.md)auf. **HrNotify** wird aufgerufen, um eine Anzeige Tabellenbenachrichtigung mit der **PR_CONTROL_ID** ([pidtagcontrolid (](pidtagcontrolid-canonical-property.md))-Eigenschaft der geänderten Eigenschaft in der [TABLE_NOTIFICATION](table_notification.md) -Struktur auszugeben. Platzieren Sie den neuen Eigenschaftswert nicht in der Struktur; Geben Sie Sie stattdessen zurück, wenn [IMAPIProp::](imapiprop-getprops.md) GetProps aufgerufen wird. Zwar kann in der Regel eine Anzeige Tabellenbenachrichtigung nicht zum Deaktivieren oder Aktivieren eines Steuerelements verwendet werden, es kann jedoch mit einer Schaltfläche verwendet werden. MAPI aktualisiert das geänderte Steuerelement so, dass es auf die Benachrichtigung reagiert. 
  
MAPI Ruft die **getlasterroraufzurufen** -Methode des Steuerelements auf, wenn **Activate** einen anderen Fehler als MAPI_E_USER_CANCEL zurückgibt. Wenn **getlasterroraufzurufen** in der [MAPIERROR](mapierror.md) -Struktur erweiterte Fehlerinformationen platziert, die im Inhalt des _lppMAPIError_ -Parameters zurückGEGEBEN werden, wird diese von MAPI für den Benutzer angezeigt. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

