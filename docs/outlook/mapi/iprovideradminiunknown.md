---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96f1c66980adebfb85b1e513df3a6ff236cf5776
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620555"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Arbeitet mit Dienstanbietern in einem Nachrichtendienst zusammen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Anbieterverwaltungsobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IProviderAdmin  <br/> |
|Zeigertyp:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](iprovideradmin-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Anbieterverwaltungsobjekt aufgetreten ist.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Bietet Zugriff auf die Anbietertabelle des Nachrichtendiensts, eine Liste der Dienstanbieter im Nachrichtendienst.  <br/> |
|[Createprovider](iprovideradmin-createprovider.md) <br/> |Fügt dem Nachrichtendienst einen Dienstanbieter hinzu.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Löscht einen Dienstanbieter aus dem Nachrichtendienst.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Öffnet einen Profilabschnitt aus dem aktuellen Profil und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Clients können einen Zeiger auf eine **IProviderAdmin-Schnittstelle** abrufen, indem sie die [IMsgServiceAdmin::AdminProviders-Methode](imsgserviceadmin-adminproviders.md) aufrufen. Dienstanbietern wird ein **IProviderAdmin-Zeiger** übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

