---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9f7667f4e1776b8aa5d6a455c847012328a35506
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567578"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Clients, Dienstanbietern und MAPI das Arbeiten mit Eigenschaften. Alle Objekte, die Eigenschaften unterstützen, implementieren diese Schnittstelle.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Kein Objekt macht diese Schnittstelle direkt verfügbar.  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen, Dienstanbieter und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProp  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROP  <br/> |
|Transaktionsmodell:  <br/> |Abstrakte Klasse, nie implementiert  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](imapiprop-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Nimmt dauerhafte Änderungen vor, die seit dem letzten Speichervorgang an einem Objekt vorgenommen wurden.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Ruft den Eigenschaftswert einer oder mehrerer Eigenschaften eines Objekts ab.  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |Gibt Eigenschaftstags für alle Eigenschaften zurück.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf eine Eigenschaft verwendet werden kann.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Aktualisiert eine oder mehrere Eigenschaften.  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Löscht eine oder mehrere Eigenschaften aus einem Objekt.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme speziell ausgeschlossener Eigenschaften.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Kopiert oder verschiebt ausgewählte Eigenschaften.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Stellt die Eigenschaftennamen bereit, die einem oder mehreren Eigenschaftsbezeichnern entsprechen.  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Stellt die Eigenschaftsbezeichner bereit, die einem oder mehreren Eigenschaftennamen entsprechen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 **IMAPIProp** ist die Basisschnittstelle für die folgenden Schnittstellen: 
  
- [IAttach](iattachimapiprop.md)
    
- [IMailUser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [IMAPIFormInfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [Imessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [IPropData](ipropdataimapiprop.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

