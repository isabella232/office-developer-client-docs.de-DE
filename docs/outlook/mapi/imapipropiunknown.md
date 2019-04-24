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
ms.openlocfilehash: 6b0a8923ee5efe22584170ce9853698885527ee8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282471"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht es Clients, Dienstanbietern und MAPI, mit Eigenschaften zu arbeiten. Alle Objekte, die Eigenschaften unterstützen, implementieren diese Schnittstelle.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Diese Schnittstelle wird von keinem Objekt direkt verfügbar gemacht.  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen, Dienstanbieter und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProp  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROP  <br/> |
|Transaktionsmodell:  <br/> |Abstrakte Klasse, nie implementiert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterroraufzurufen](imapiprop-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Macht alle Änderungen, die an einem Objekt seit dem letzten Speichervorgang vorgenommen wurden, dauerhaft.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Ruft den Eigenschaftswert einer oder mehrerer Eigenschaften eines Objekts ab.  <br/> |
|[GetProplist](imapiprop-getproplist.md) <br/> |Gibt Eigenschaftentags für alle Eigenschaften zurück.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf eine Eigenschaft verwendet werden kann.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Aktualisiert eine oder mehrere Eigenschaften.  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Löscht eine oder mehrere Eigenschaften aus einem Objekt.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme der explizit ausgeschlossenen Eigenschaften.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Kopiert oder verschiebt ausgewählte Eigenschaften.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Stellt die Eigenschaftennamen bereit, die einem oder mehreren Eigenschafts Bezeichnern entsprechen.  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Stellt die Eigenschaftenbezeichner bereit, die einem oder mehreren Eigenschaftsnamen entsprechen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 **IMAPIProp** ist die Basisschnittstelle für die folgenden Schnittstellen: 
  
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

