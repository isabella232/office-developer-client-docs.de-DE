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
ms.openlocfilehash: 21889bf626d7f9128d1e01b3e6a15b5fa0d2e696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792643"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**Betrifft**: Outlook 
  
Ändert eine Message Service in einem Profil.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |MapiX.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Message Service Administration-Objekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Zeigertyp:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über die letzten von einem Objekt "Message" Service Administration generierten Fehler enthält.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Bietet Zugriff auf die Nachricht Service Tabelle eine Liste der Nachrichtendienste im Profil.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Fügt einen Nachrichtendienst zum aktuellen Profil hinzu.  <br/> <br/>**Hinweis**: Diese Methode ist veraltet. Verwenden Sie stattdessen [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) .           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Löscht eine Message Service aus einem Profil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Kopiert eine Message Service in einem Profil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Veraltet. Weist einen neuen Namen zu einem Nachrichtendienst.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Konfiguriert einen Message-Dienst neu.  <br/> |
|["OpenProfileSection"](imsgserviceadmin-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen Zeiger [IProfSect](iprofsectimapiprop.md) für den weiteren Zugriff.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Legt die Reihenfolge, in welcher, die Transport Anbieter aufgerufen werden, um eine Nachricht zu übermitteln.  <br/> |
|["AdminProviders"](imsgserviceadmin-adminproviders.md) <br/> |Gibt einen Zeiger, der Zugriff auf ein Anbieter Administration-Objekt bietet.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Legt eine Message Service hat der Hersteller der primäre Identität für das Profil sein.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Bietet Zugriff auf die Tabelle Dienstanbieter, eine Liste der Dienstanbieter im Profil.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine Implementierung kann einen Zeiger auf eine **IMsgServiceAdmin** -Schnittstelle auf zwei Arten erhalten: durch Aufrufen der [IMAPISession::AdminServices](imapisession-adminservices.md) -Methode oder durch Aufrufen der [IProfAdmin::AdminServices](iprofadmin-adminservices.md) -Methode. Für Clients hauptsächlich Profilkonfiguration ist **IProfAdmin::AdminServices** die bevorzugte Methode zum Abrufen der **IMsgServiceAdmin** -Schnittstelle, weil es nicht auf den Anbieter für die MAPI-Sitzung anmelden ist. Benötigt ein Client die Möglichkeit, das aktive Profil ändern, sollte **IMAPISession::AdminServices** aufgerufen werden, wenn den Mauszeiger **IMsgServiceAdmin** erhalten möchten. Beachten Sie, dass zwar MAPI nicht mit einem Profil zulässt, die zu löschenden verwendet wird, keine Sicherheitsmaßnahmen werden, um zu verhindern, dass einen Client die Message-Dienste im Profil entfernen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

