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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 559680b9ca4ea5be85718d8f9692df93f77b0edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585752"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Funktioniert mit-Dienstanbieter in einem Message-Dienst. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verfügbar gemacht von:  <br/> |Verwaltungsobjekte Anbieter  <br/> |
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Clients können einen Zeiger auf eine **IProviderAdmin** -Schnittstelle abrufen, indem Sie die [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) -Methode aufrufen; Dienstanbieter sind ein **IProviderAdmin** -Zeiger übergeben, wenn ihre Messagingdiensts Entry Point-Funktion aufgerufen wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

