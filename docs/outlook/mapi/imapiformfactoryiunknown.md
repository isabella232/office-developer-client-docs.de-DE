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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342119"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt die Verwendung von konfigurierbaren Lauf Zeit Formularen in verteilten Computerumgebungen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formular Factory-Objekte  <br/> |
|Implementiert von:  <br/> |Formularserver  <br/> |
|Aufgerufen von:  <br/> |Formular Betrachter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormFactory  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Gibt ein klassenfactoryobjekt für das Formular zurück.  <br/> |
|[Getlasterroraufzurufen](imapiformfactory-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der für das Form Factory-Objekt auftritt.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Hält einen geöffneten Formularserver im Arbeitsspeicher.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFormFactory** -Schnittstelle basiert auf der [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) -Schnittstelle, und Objekte, die **IMAPIFormFactory** implementieren, sollten auch von **IClassFactory**erben.
  
 **IMAPIFormFactory** ist die Schnittstelle, die Formular Betrachter zum Erstellen neuer Formularobjekte verwenden, wenn ein Formularserver mehr als eine Nachrichtenklasse unterstützt (also mehr als einen Formular Objekttyp). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

