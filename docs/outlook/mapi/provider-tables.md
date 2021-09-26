---
title: Anbietertabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d68e27f0d34be17fadbb1c99150e767f6e10b13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599179"
---
# <a name="provider-tables"></a>Anbietertabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Anbietertabelle enthält Informationen zu Dienstanbietern. Es gibt zwei verschiedene Anbietertabellen, die sowohl von mapi implementiert als auch von Clients verwendet werden. Die erste Tabelle, auf die durch Aufrufen der [IMsgServiceAdmin::GetProviderTable-Methode](imsgserviceadmin-getprovidertable.md) zugegriffen wird, enthält Informationen zu allen Anbietern für das aktuelle Profil. Die zweite Tabelle, auf die über [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)zugegriffen wird, erstellt eine Tabelle, in der Informationen zu allen Dienstanbietern für einen Nachrichtendienst gespeichert werden.
  
Diese beiden Tabellen weisen einen weiteren Unterschied auf. Die über **IMsgServiceAdmin::GetProviderTable** verfügbare Anbietertabelle enthält nur Zeilen, die Dienstanbieter darstellen, während die über **IProviderAdmin::GetProviderTable** verfügbare Tabelle Zeilen enthalten kann, die zusätzliche Informationen darstellen, die einem Dienstanbieter zugeordnet sind. Diese zusätzlichen Informationen werden dem Profil mit dem Schlüsselwort "Sections" von MAPISVC.INF hinzugefügt. Wenn ein Anbieter über zusätzliche Profilabschnitte verfügt, werden die **MAPIUID-Werte** für diese Abschnitte in der **Eigenschaft PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) gespeichert. **PR_SERVICE_EXTRA_UIDS** wird im Abschnitt "Nachrichtendienstprofil" gespeichert. 
  
Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in beiden Arten von Anbietertabellen:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
Die Anbietertabelle kann verwendet werden, um die aktuelle Transportreihenfolge anzuzeigen oder zu ändern. Um die aktuelle Reihenfolge anzuzeigen, erstellen Sie eine Einschränkung, um nur die Zeilen abzurufen, deren **PR_RESOURCE_TYPE** Eigenschaft auf MAPI_TRANSPORT_PROVIDER festgelegt ist. Verwenden Sie dann **PR_PROVIDER_ORDINAL** als Sortierschlüssel, um die Tabelle zu sortieren und alle Zeilen mit der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) oder der [HrQueryAllRows-Funktion](hrqueryallrows.md) abzurufen. 
  
Um die Transportreihenfolge zu ändern, wenden Sie die gleiche Einschränkung an, und rufen Sie die Zeilen ab. Erstellen Sie dann ein Array von Werten aus der **PR_PROVIDER_UID** Eigenschaft, die die eindeutigen Bezeichner für die Transportanbieter darstellt. Wenn sich die Bezeichner in der gewünschten Reihenfolge befinden, übergeben Sie sie an die [IMsgServiceAdmin::MsgServiceTransportOrder-Methode.](imsgserviceadmin-msgservicetransportorder.md) 
  
Nachdem eine Anbietertabelle zur Verfügung gestellt wurde, werden nachfolgende Änderungen, z. B. das Hinzufügen oder Löschen eines Anbieters, nicht angezeigt.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

