---
title: Anbieter Tabellen
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
# <a name="provider-tables"></a>Anbieter Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Anbieter Tabelle enthält Informationen zu Dienstanbietern. Es gibt zwei verschiedene Anbieter Tabellen, die von MAPI implementiert und von Clients verwendet werden. Die erste Tabelle, auf die durch Aufrufen der [IMsgServiceAdmin:: GetProvider](imsgserviceadmin-getprovidertable.md) Table-Methode zugegriffen wird, enthält Informationen zu allen Anbietern für das aktuelle Profil. In der zweiten Tabelle, auf die über [IProviderAdmin::](iprovideradmin-getprovidertable.md)getproviderable zugegriffen wird, wird eine Tabelle erstellt, in der Informationen zu allen Dienstanbietern für einen Nachrichtendienst gespeichert werden.
  
Diese beiden Tabellen haben einen weiteren Unterschied. Die Anbieter Tabelle, die über **IMsgServiceAdmin::** getproviderable verfügbar ist, enthält nur Zeilen, die Dienstanbieter darstellen, während die über **IProviderAdmin::** getproviderable verfügbare Tabelle Zeilen enthalten kann, die zusätzliche Informationen, die einem Dienstanbieter zugeordnet sind. Diese zusätzlichen Informationen werden dem Profil mit dem Schlüsselwort "Sections" von MAPISVC. INF hinzugefügt. Wenn ein Anbieter über zusätzliche Profilabschnitte verfügt, speichert er die **MAPIUID** -Werte für diese Abschnitte in der **PR_SERVICE_EXTRA_UIDS** ([pidtagserviceextrauids (](pidtagserviceextrauids-canonical-property.md))-Eigenschaft. **PR_SERVICE_EXTRA_UIDS** wird im Abschnitt Nachrichtendienst Profil gespeichert. 
  
Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in beiden Typen von Anbieter Tabellen:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([Pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([Pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([Pidtagproviderordinal (](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([Pidtagprovideruid (](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([Pidtagservicename (](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([Pidtagserviceuid (](pidtagserviceuid-canonical-property.md))  <br/> |
   
Die Anbieter Tabelle kann verwendet werden, um den aktuellen Transportauftrag anzuzeigen oder zu ändern. Um die aktuelle Reihenfolge anzuzeigen, erstellen Sie eine Einschränkung, um nur die Zeilen abzurufen, deren **PR_RESOURCE_TYPE** -Eigenschaft auf MAPI_TRANSPORT_PROVIDER festgelegt ist. Verwenden Sie dann **PR_PROVIDER_ORDINAL** als Sortierschlüssel, um die Tabelle zu sortieren und alle Zeilen mit der [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode oder der [HrQueryAllRows](hrqueryallrows.md) -Funktion abzurufen. 
  
Um den Transportauftrag zu ändern, wenden Sie dieselbe Einschränkung an, und rufen Sie die Zeilen ab. Erstellen Sie dann ein Array mit Werten aus der **PR_PROVIDER_UID** -Eigenschaft, die die eindeutigen Bezeichner für die Transportanbieter darstellt. Wenn die Bezeichner in der gewünschten Reihenfolge vorliegen, müssen Sie Sie an die [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) -Methode weitergeben. 
  
Nachdem eine Anbieter Tabelle verfügbar gemacht wurde, werden nachfolgende Änderungen, wie das Hinzufügen oder Löschen eines Anbieters, nicht wiedergegeben.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

