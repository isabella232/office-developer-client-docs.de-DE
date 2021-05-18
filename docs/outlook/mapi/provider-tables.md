---
title: Anbietertabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408971"
---
# <a name="provider-tables"></a>Anbietertabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Anbietertabelle enthält Informationen zu Dienstanbietern. Es gibt zwei verschiedene Anbietertabellen, die beide von MAPI implementiert und von Clients verwendet werden. Die erste Tabelle, auf die durch Aufrufen der [IMsgServiceAdmin::GetProviderTable-Methode](imsgserviceadmin-getprovidertable.md) zugegriffen wird, enthält Informationen zu allen Anbietern für das aktuelle Profil. In der zweiten Tabelle, auf die über [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)zugegriffen wird, wird eine Tabelle erstellt, in der Informationen zu allen Dienstanbietern für einen Nachrichtendienst enthalten sind.
  
Diese beiden Tabellen haben einen weiteren Unterschied. Die über **IMsgServiceAdmin::GetProviderTable** verfügbare Anbietertabelle enthält nur Zeilen, die Dienstanbieter darstellen, während die über **IProviderAdmin::GetProviderTable** verfügbare Tabelle Zeilen enthalten kann, die zusätzliche Informationen darstellen, die einem Dienstanbieter zugeordnet sind. Diese zusätzlichen Informationen werden dem Profil mit dem Schlüsselwort "Sections" von MAPISVC.INF hinzugefügt. Wenn ein Anbieter über zusätzliche Profilabschnitte verfügt, speichert er die **MAPIUID-Werte** für diese Abschnitte in der **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) -Eigenschaft. **PR_SERVICE_EXTRA_UIDS** wird im Abschnitt Nachrichtendienstprofil gespeichert. 
  
Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in beiden Typen von Anbietertabellen zusammen:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
Die Anbietertabelle kann zum Anzeigen der aktuellen Transportreihenfolge oder zum Ändern verwendet werden. Erstellen Sie zum Anzeigen der aktuellen Reihenfolge eine Einschränkung, um nur die Zeilen abzurufen, deren **PR_RESOURCE_TYPE** auf MAPI_TRANSPORT_PROVIDER. Verwenden Sie **PR_PROVIDER_ORDINAL** sortiertaste, um die Tabelle zu sortieren und alle Zeilen mit der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) oder der [HrQueryAllRows-Funktion](hrqueryallrows.md) abzurufen. 
  
Um die Transportreihenfolge zu ändern, wenden Sie dieselbe Einschränkung an, und rufen Sie die Zeilen ab. Erstellen Sie dann ein Array  von Werten aus der PR_PROVIDER_UID-Eigenschaft, die die eindeutigen Bezeichner für die Transportanbieter darstellt. Wenn sich die Bezeichner in der gewünschten Reihenfolge befinden, übergeben Sie sie an die [IMsgServiceAdmin::MsgServiceTransportOrder-Methode.](imsgserviceadmin-msgservicetransportorder.md) 
  
Nachdem eine Anbietertabelle verfügbar gemacht wurde, werden nachfolgende Änderungen, z. B. das Hinzu- oder Löschen eines Anbieters, nicht mehr angezeigt.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

