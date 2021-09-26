---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d9ab1c92faa2780680d198939712163a79e3b3ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610601"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt die Verwendung konfigurierbarer Laufzeitformulare in verteilten Computerumgebungen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formularfactoryobjekte  <br/> |
|Implementiert von:  <br/> |Formularserver  <br/> |
|Aufgerufen von:  <br/> |Formularanzeigen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormFactory  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Gibt ein Klassenfactoryobjekt für das Formular zurück.  <br/> |
|[Getlasterror](imapiformfactory-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Formularfactoryobjekt aufgetreten ist.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Behält einen geöffneten Formularserver im Arbeitsspeicher bei.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFormFactory-Schnittstelle** basiert auf der [IClassFactory-Schnittstelle,](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) und Objekte, die **IMAPIFormFactory** implementieren, sollten ebenfalls von **IClassFactory erben.**
  
 **IMAPIFormFactory** ist die Schnittstelle, die Formularviewer verwenden, um neue Formularobjekte zu erstellen, wenn ein Formularserver mehrere Nachrichtenklassen unterstützt (d. b. mehrere Formularobjekttypen). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

