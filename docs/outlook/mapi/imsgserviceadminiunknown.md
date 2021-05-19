---
title: IMsgServiceAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin
api_type:
- COM
ms.assetid: 5905b9e9-c462-451d-a49f-1f3a8aa506a6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aba61d4acf7c1f9a5d91fa15f1ca6b16f173bcb2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426135"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nimmt Änderungen an einem Nachrichtendienst in einem Profil vor.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |MapiX.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtendienstverwaltungsobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Zeigertyp:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum letzten Fehler enthält, der von einem Nachrichtendienstverwaltungsobjekt generiert wurde.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Bietet Zugriff auf die Nachrichtendiensttabelle, eine Liste der Nachrichtendienste im Profil.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Fügt dem aktuellen Profil einen Nachrichtendienst hinzu.  <br/> <br/>**HINWEIS**: Diese Methode ist veraltet. Verwenden [Sie stattdessen IMsgServiceAdmin2::CreateMsgServiceEx.](imsgserviceadmin2-createmsgserviceex.md)           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Löscht einen Nachrichtendienst aus einem Profil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Kopiert einen Nachrichtendienst in ein Profil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Veraltet. Weist einem Nachrichtendienst einen neuen Namen zu.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Konfiguriert einen Nachrichtendienst neu.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Legt die Reihenfolge fest, in der Transportanbieter aufgerufen werden, um eine Nachricht zu senden.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Gibt einen Zeiger zurück, der Zugriff auf ein Anbieterverwaltungsobjekt bietet.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Bestimmt einen Nachrichtendienst als Anbieter der primären Identität für das Profil.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Bietet Zugriff auf die Anbietertabelle, eine Auflistung der Dienstanbieter im Profil.  <br/> |
   
## <a name="remarks"></a>Hinweise

Eine Implementierung kann einen Zeiger auf eine **IMsgServiceAdmin-Schnittstelle** auf zwei Arten erhalten: durch Aufrufen der [IMAPISession::AdminServices-Methode](imapisession-adminservices.md) oder durch Aufrufen der [IProfAdmin::AdminServices-Methode.](iprofadmin-adminservices.md) Für Clients, die in erster Linie mit der Profilkonfiguration betroffen sind, ist **IProfAdmin::AdminServices** die bevorzugte Methode, um die **IMsgServiceAdmin-Schnittstelle zu** erhalten, da sie sich nicht bei Anbietern bei der MAPI-Sitzung anmeldet. Wenn ein Client änderungen am aktiven Profil vornehmen muss, sollte **IMAPISession::AdminServices** aufgerufen werden, um den **IMsgServiceAdmin-Zeiger zu** erhalten. Beachten Sie, dass mapi zwar nicht zu lässt, dass ein verwendetes Profil gelöscht wird, es aber keine Garantien gibt, die verhindern, dass ein Client alle Nachrichtendienste im Profil entfernt. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

