---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342119"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt die Verwendung konfigurierbarer Laufzeitformulare in verteilten Computerumgebungen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Form Factory-Objekte  <br/> |
|Implementiert von:  <br/> |Formularserver  <br/> |
|Aufgerufen von:  <br/> |Formularanzeigen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormFactory  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Gibt ein Klassen factory-Objekt für das Formular zurück.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Form Factory-Objekt aufgetreten ist.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Behält einen geöffneten Formularserver im Arbeitsspeicher bei.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **IMAPIFormFactory-Schnittstelle** basiert auf der [IClassFactory-Schnittstelle,](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) und Objekte, die **IMAPIFormFactory** implementieren, sollten auch von **IClassFactory erben.**
  
 **IMAPIFormFactory** ist die Schnittstelle, mit der Formularanzeigen neue Formularobjekte erstellen, wenn ein Formularserver mehrere Nachrichtenklassen unterstützt (d. h. mehr als einen Formularobjekttyp). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

