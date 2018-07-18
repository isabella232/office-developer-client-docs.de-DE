---
title: Anbietertabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a613bd744a113b4378c5bef94fb51f6ae3aa4041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795330"
---
# <a name="provider-tables"></a>Anbietertabellen

  
  
**Betrifft**: Outlook 
  
Eine Anbieter-Tabelle enthält Informationen zu Dienstanbietern. Es gibt zwei verschiedene Anbieter Tabellen, beide MAPI implementiert und von Clients verwendet wird. Die erste Tabelle, die durch Aufrufen der Methode [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) zugegriffen enthält Informationen über alle Anbieter für das aktuelle Profil. Die zweite Tabelle, auf die Sie über [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), erstellt eine Tabelle, die Informationen zu allen-Dienstanbieter für einen Nachrichtendienst gespeichert.
  
Diese beiden Tabellen haben ein weiterer Unterschied. Tabelle der Dienstanbieter über **IMsgServiceAdmin::GetProviderTable** verfügbar enthält nur die Zeilen, die Dienstanbieter darstellen, während die Tabelle über **IProviderAdmin::GetProviderTable** Zeilen hinzugefügt werden, die darstellen Weitere Informationen im Zusammenhang mit einem Dienstanbieter. Diese zusätzlichen Informationen wird das Profil mit dem Schlüsselwort "Abschnitte" der MAPISVC.INF hinzugefügt. Wenn ein Anbieter zusätzliche Profil hat, werden die **MAPIUID** Werte für diese Abschnitte in der Eigenschaft **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) gespeichert. **PR_SERVICE_EXTRA_UIDS** wird im Abschnitt Profile Service Nachricht gespeichert. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte in beide Arten von Anbieter für Tabellen festzulegen:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
Tabelle der Dienstanbieter kann verwendet werden, um die aktuelle Transport Reihenfolge anzuzeigen oder zu ändern. Um die aktuelle Reihenfolge anzuzeigen, erstellen Sie eine Einschränkung, um nur die Zeilen mit der **PR_RESOURCE_TYPE** -Eigenschaft, um MAPI_TRANSPORT_PROVIDER abzurufen. Klicken Sie dann verwenden Sie **PR_PROVIDER_ORDINAL** als Sortierschlüssel zum Sortieren der Tabelle und alle Zeilen mit [der QueryRows](imapitable-queryrows.md) oder die Funktion [HrQueryAllRows](hrqueryallrows.md) abrufen. 
  
Ändern der Reihenfolge Transport, gelten diese Beschränkung und die Zeilen abrufen. Klicken Sie dann erstellen Sie ein Array von Werten aus der **PR_PROVIDER_UID** -Eigenschaft, die die eindeutigen Bezeichner für den Transport Anbietern darstellt. Wenn der Bezeichner in der gewünschten Reihenfolge befinden, an die [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) -Methode übergeben. 
  
Nachdem eine Tabelle Anbieter verfügbar gemacht wurde, wird es nicht nachfolgende Änderungen, wie die Hinzufügung oder Löschung eines Anbieters wider.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

