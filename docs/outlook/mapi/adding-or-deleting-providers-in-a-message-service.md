---
title: Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ed5ea8bdfcbdaaa6b6abd81a39f0e8df50d3b314
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433423"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwenden Sie zum Hinzufügen oder Löschen von Dienstanbietern in einem Nachrichtendienst die [IProviderAdmin : IUnknown-Schnittstelle.](iprovideradminiunknown.md) Sie können einen **IProviderAdmin-Zeiger abrufen,** indem Sie [IMsgServiceAdmin::AdminProviders aufrufen.](imsgserviceadmin-adminproviders.md) In der Anbietertabelle, auf die über [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)zugegriffen werden kann, werden Informationen zu den derzeit im Nachrichtendienst installierten Dienstanbietern aufgeführt. Clients und Dienstanbieter können die Anbietertabelle verwenden, um beispielsweise auf den Namen der Anbieter-DLL-Datei oder die **MAPIUID,** den Anzeigenamen und den Typ des Anbieters sowie Informationen zum Nachrichtendienst zu zugreifen. Weitere Informationen finden Sie unter [Anbietertabellen](provider-tables.md).
  
 **So fügen Sie einen Dienstanbieter in einem Nachrichtendienst hinzu oder löschen ihn**
  
1. Rufen Sie die **AdminServices-Methode** auf, um auf ein Nachrichtendienstverwaltungsobjekt zu zugreifen. 
    
2. Rufen [Sie IMsgServiceAdmin::GetMsgServiceTable auf,](imsgserviceadmin-getmsgservicetable.md) um auf die Nachrichtendiensttabelle zu zugreifen. 
    
3. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) mit dem Namen des zu ändernden Nachrichtendiensts entspricht. 
    
4. Rufen Sie die [IMAPITable::FindRow-Methode](imapitable-findrow.md) der Nachrichtendiensttabelle auf, um die Zeile in der Tabelle zu finden, die den zielorientierten Nachrichtendienst darstellt. 
    
5. Rufen [Sie IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) auf, um einen **IProviderAdmin-Zeiger abzurufen.** Übergeben Sie **die PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) aus der Zeile nachrichtendiensttabelle als _lpUID-Parameter._ 
    
6. Rufen [Sie IProviderAdmin::GetProviderTable auf,](iprovideradmin-getprovidertable.md) um auf die Anbietertabelle zu zugreifen. 
    
7. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer SPropertyRestriction-Struktur, die **mit PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) mit dem Namen des Dienstanbieters, der hinzugefügt oder gelöscht werden soll, entspricht. 
    
8. Rufen Sie die [IMAPITable::FindRow-Methode](imapitable-findrow.md) der Anbietertabelle auf, um die Zeile in der Tabelle zu finden, die den zielorientierten Dienstanbieter darstellt. 
    
9. Rufen [Sie IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md) auf, um den Anbieter oder [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md) hinzuzufügen, um ihn aus dem Nachrichtendienst zu entfernen. Übergeben **Sie für CreateProvider** die **PR_DISPLAY_NAME** des Anbieters als _lpszProvider-Parameter._ Übergeben Sie für beide Methoden die PR_SERVICE_UID **des** Anbieters als _lpUID-Parameter._ Nachdem der Dienstanbieter hinzugefügt oder gelöscht wurde, wird die Änderung erst sichtbar, wenn eine neue Sitzung erstellt wurde. 
    
Eine weitere Methode zum Hinzufügen eines Dienstanbieters, insbesondere eines Nachrichtenspeicheranbieters, zu einem Profil besteht darin, eine Eintrags-ID für den Anbieter zu erstellen. Da das Erstellen einer Eintrags-ID Kenntnisse über ihr Format erfordert, kann diese Technik nur verwendet werden, wenn der Dienstanbieter sein Eingabebezeichnerformat öffentlich gemacht hat. 
  
Mit dem neu erstellten Eintragsbezeichner kann ein Client [IMAPISession::OpenMsgStore aufrufen.](imapisession-openmsgstore.md) MAPI erstellt automatisch einen Profilabschnitt im Profil für den Dienstanbieter, fügt ihn jedoch nicht einem Nachrichtendienst hinzu. 
  
Einige Nachrichtendienste lassen diese Art von dynamischen Änderungen nicht zu. Ob dies unterstützt wird, liegt beim Nachrichtendienst. Ein weiteres Feature, das möglicherweise unterstützt wird, ist die Möglichkeit, direkt auf die privaten Profilabschnitte eines Nachrichtendiensts zu zugreifen. Wenn der von Ihnen verwendete Nachrichtendienst diesen Zugriff zulässt, veröffentlicht er die **GUID,** die den privaten Abschnitt in MAPISVC.INF darstellt. Sie können diese **GUID** in einem Aufruf an [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) übergeben, um auf den Profilabschnitt zu zugreifen. 
  

