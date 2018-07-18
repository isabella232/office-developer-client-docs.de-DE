---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 41195a49d1bf3566c81fe6e97697012209cbc5ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792776"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Betrifft**: Outlook 
  
Funktioniert mit-Dienstanbieter in einem Message-Dienst. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Verwaltungsobjekte Anbieter  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IProviderAdmin  <br/> |
|Zeigertyp:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält, die für den Anbieter Verwaltungsobjekt aufgetreten ist.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Bietet Zugriff auf den Dienst Anbieter Tabelle, eine Liste der Dienstanbieter in der Nachrichtendienst.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Fügt einen Dienstanbieter an den Dienst.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Löscht einen Dienstanbieter aus der Nachrichtendienst.  <br/> |
|["OpenProfileSection"](iprovideradmin-openprofilesection.md) <br/> |Öffnet einen Profilabschnitt aus dem aktuellen Profil, und gibt einen [IProfSect](iprofsectimapiprop.md) Zeiger für den weiteren Zugriff.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Clients können einen Zeiger auf eine **IProviderAdmin** -Schnittstelle abrufen, indem Sie die [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) -Methode aufrufen; Dienstanbieter sind ein **IProviderAdmin** -Zeiger übergeben, wenn ihre Messagingdiensts Entry Point-Funktion aufgerufen wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

