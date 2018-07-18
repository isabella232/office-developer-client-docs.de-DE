---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 02d2b136ed1437ba53ce1e54a202d70a48b2abe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792296"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**Betrifft**: Outlook 
  
Ermöglicht es Clients, Service Provider und MAPI-Eigenschaften entwickelt. Alle Objekte, Eigenschaften unterstützen, implementieren Sie diese Schnittstelle.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Kein Objekt macht diese Schnittstelle direkt verfügbar.  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen, Service Provider und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProp  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROP  <br/> |
|Transaktionsmodell:  <br/> |Abstrakte Basisklasse, die nie implementiert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Macht dauerhaft entfernt alle Änderungen, die seit dem letzten Speichervorgang auf ein Objekt vorgenommen wurden.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Ruft den Wert der Eigenschaft um, der eine oder mehrere Eigenschaften eines Objekts an.  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |Eigenschaftentags für alle Eigenschaften zurückgegeben.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Gibt einen Zeiger auf eine Schnittstelle, die Zugriff auf eine Eigenschaft verwendet werden können.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Aktualisiert eine oder mehrere Eigenschaften.  <br/> |
|["DeleteProps"](imapiprop-deleteprops.md) <br/> |Löscht eine oder mehrere Eigenschaften aus einem Objekt.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme von speziell Ausgeschlossene Eigenschaften.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Kopiert oder verschiebt ausgewählten Eigenschaften.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Enthält die Eigenschaftennamen, die einen oder mehrere Eigenschaftenbezeichner entsprechen.  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Enthält die Eigenschaftenbezeichner, die mindestens einen Eigenschaftennamen entsprechen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 **IMAPIProp** ist die Basis-Schnittstelle für die folgenden Schnittstellen: 
  
- [IAttach](iattachimapiprop.md)
    
- [IMailUser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [IMAPIFormInfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [IMessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [IPropData](ipropdataimapiprop.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

