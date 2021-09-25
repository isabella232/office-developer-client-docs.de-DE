---
title: IMsgServiceAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin
api_type:
- COM
ms.assetid: 5905b9e9-c462-451d-a49f-1f3a8aa506a6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e4c66a4a06cbfb3907053aead043c03dcb0cfe60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579866"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nimmt Änderungen an einem Nachrichtendienst in einem Profil vor.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |MapiX.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtendienst-Verwaltungsobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Zeigertyp:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](imsgserviceadmin-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen über den letzten Fehler enthält, der von einem Nachrichtendienst-Verwaltungsobjekt generiert wurde.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Ermöglicht den Zugriff auf die Nachrichtendiensttabelle, eine Liste der Nachrichtendienste im Profil.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Fügt dem aktuellen Profil einen Nachrichtendienst hinzu.  <br/> <br/>**HINWEIS:** Diese Methode ist veraltet. Verwenden Sie stattdessen [IMsgServiceAdmin2::CreateMsgServiceEx.](imsgserviceadmin2-createmsgserviceex.md)           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Löscht einen Nachrichtendienst aus einem Profil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Kopiert einen Nachrichtendienst in ein Profil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Veraltet. Weist einem Nachrichtendienst einen neuen Namen zu.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Konfiguriert einen Nachrichtendienst neu.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Legt die Reihenfolge fest, in der Transportanbieter aufgerufen werden, um eine Nachricht zuzustellen.  <br/> |
|[AdminProvider](imsgserviceadmin-adminproviders.md) <br/> |Gibt einen Zeiger zurück, der Zugriff auf ein Anbieterverwaltungsobjekt bietet.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Legt einen Nachrichtendienst als Lieferanten der primären Identität für das Profil.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Ermöglicht den Zugriff auf die Anbietertabelle, eine Auflistung der Dienstanbieter im Profil.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Eine Implementierung kann auf zwei Arten einen Zeiger auf eine **IMsgServiceAdmin-Schnittstelle** abrufen: durch Aufrufen der [IMAPISession::AdminServices-Methode](imapisession-adminservices.md) oder durch Aufrufen der [IProfAdmin::AdminServices-Methode.](iprofadmin-adminservices.md) Für Clients, die in erster Linie mit der Profilkonfiguration befasst sind, ist **IProfAdmin::AdminServices** die bevorzugte Methode zum Abrufen der **IMsgServiceAdmin-Schnittstelle,** da sie keine Anbieter bei der MAPI-Sitzung anmeldet. Wenn ein Client die Möglichkeit benötigt, Änderungen am aktiven Profil vorzunehmen, sollte **IMAPISession::AdminServices** aufgerufen werden, um den **IMsgServiceAdmin-Zeiger** abzurufen. Beachten Sie, dass zwar die MAPI das Löschen eines verwendeten Profils nicht zulässt, es jedoch keine Sicherheitsmaßnahmen gibt, um zu verhindern, dass ein Client alle Nachrichtendienste im Profil entfernt. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

