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
ms.openlocfilehash: b2aa08ea14df87f24cda3da0137ae4bfa2c50b40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576015"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Unterstützt die Verwendung von konfigurierbar Laufzeit-Formularen in einer verteilten Umgebung Netzwerke. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verfügbar gemacht von:  <br/> |Formular Factory-Objekte  <br/> |
|Implementiert von:  <br/> |Formular-Servern  <br/> |
|Aufgerufen von:  <br/> |Formular-Viewer  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormFactory  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Gibt ein Klasse Factory-Objekt für das Formular.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, auf das Formular Factory-Objekt enthält.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Wird einen geöffnete Formular Server im Arbeitsspeicher gespeichert.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Schnittstelle **IMAPIFormFactory** basiert auf der [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) -Schnittstelle und Objekte, die **IMAPIFormFactory** implementieren sollten auch von **IClassFactory**erben.
  
 **IMAPIFormFactory** ist die Schnittstelle, die Formular Viewer verwenden, um die neue Formularobjekte zu erstellen, wenn ein Formular Server mehr als eine Nachrichtenklasse unterstützt (d. h., mehrere Typ der Form-Objekt). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

