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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aba61d4acf7c1f9a5d91fa15f1ca6b16f173bcb2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309709"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nimmt Änderungen an einem Nachrichtendienst in einem Profil vor.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |MapiX. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Nachrichtendienst-Verwaltungsobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Zeigertyp:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterroraufzurufen](imsgserviceadmin-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum letzten Fehler enthält, der von einem Nachrichtendienst-Verwaltungsobjekt generiert wurde.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Ermöglicht den Zugriff auf die Nachrichtendienst Tabelle, eine Liste der Nachrichtendienste im Profil.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Fügt dem aktuellen Profil einen Nachrichtendienst hinzu.  <br/> <br/>**Hinweis**: Diese Methode ist veraltet. Verwenden Sie stattdessen [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) .           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Löscht einen Nachrichtendienst aus einem Profil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Kopiert einen Nachrichtendienst in ein Profil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Veraltet. Weist einem Nachrichtendienst einen neuen Namen zu.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Konfiguriert einen Nachrichtendienst neu.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für den weiteren Zugriff zurück.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Legt die Reihenfolge fest, in der Transportanbieter aufgerufen werden, um eine Nachricht zu übermitteln.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Gibt einen Zeiger zurück, der Zugriff auf ein Anbieter Verwaltungsobjekt bereitstellt.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Legt fest, dass ein Nachrichtendienst der Lieferant der primären Identität für das Profil ist.  <br/> |
|[GetProviderable](imsgserviceadmin-getprovidertable.md) <br/> |Ermöglicht den Zugriff auf die Anbieter Tabelle, eine Liste der Dienstanbieter im Profil.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine Implementierung kann einen Zeiger auf eine **IMsgServiceAdmin** -Schnittstelle auf zweierlei Weise abrufen: durch Aufrufen der [IMAPISession:: AdminServices](imapisession-adminservices.md) -Methode oder durch Aufrufen der [IProfAdmin:: AdminServices](iprofadmin-adminservices.md) -Methode. Für Clients, die sich hauptsächlich mit der Profilkonfiguration befassen, ist **IProfAdmin:: AdminServices** die bevorzugte Methode zum Abrufen der **IMsgServiceAdmin** -Schnittstelle, da Sie keine Anbieter für die MAPI-Sitzung anmeldet. Wenn ein Client die Möglichkeit zum Ändern des aktiven Profils erfordert, sollte **IMAPISession:: AdminServices** aufgerufen werden, um den **IMsgServiceAdmin** -Zeiger abzurufen. Beachten Sie, dass MAPI zwar nicht zulässt, dass ein Profil, das verwendet wird, gelöscht wird, es gibt jedoch keine Sicherheitsvorkehrungen, um zu verhindern, dass ein Client alle Nachrichtendienste im Profil entfernt. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

