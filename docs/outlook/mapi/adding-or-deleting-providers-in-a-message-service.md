---
title: Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1b29714e4cc61f628fb7093be609bfdb63763fb1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588259"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwenden Sie zum Hinzufügen oder Löschen von Dienstanbietern in einem Nachrichtendienst die [IProviderAdmin : IUnknown-Schnittstelle.](iprovideradminiunknown.md) Sie können einen **IProviderAdmin-Zeiger** abrufen, indem [Sie IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)aufrufen. In der Anbietertabelle, auf die über [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)zugegriffen werden kann, sind Informationen zu den derzeit im Nachrichtendienst installierten Dienstanbietern aufgeführt. Clients und Dienstanbieter können die Anbietertabelle verwenden, um auf den Namen der Anbieter-DLL-Datei zuzugreifen, z. B. **MAPIUID,** Anzeigename und Anbietertyp sowie Informationen zum Nachrichtendienst. Weitere Informationen finden Sie unter [Anbietertabellen.](provider-tables.md)
  
 **So fügen Sie einen Dienstanbieter zu einem Nachrichtendienst hinzu oder löschen diesen**
  
1. Rufen Sie die **AdminServices-Methode** auf, um auf ein Nachrichtendienst-Verwaltungsobjekt zuzugreifen. 
    
2. Rufen Sie [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) auf, um auf die Nachrichtendiensttabelle zuzugreifen. 
    
3. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) mit dem Namen des zu ändernden Nachrichtendiensts entspricht. 
    
4. Rufen Sie die [IMAPITable::FindRow-Methode](imapitable-findrow.md) der Nachrichtendiensttabelle auf, um die Zeile in der Tabelle zu suchen, die den Zielnachrichtendienst darstellt. 
    
5. Rufen Sie [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) auf, um einen **IProviderAdmin-Zeiger** abzurufen. Übergeben Sie die **Spalte PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) aus der Tabellenzeile des Nachrichtendiensts als _lpUID-Parameter._ 
    
6. Rufen [Sie IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) auf, um auf die Anbietertabelle zuzugreifen. 
    
7. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer SPropertyRestriction-Struktur, die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) mit dem Namen des Dienstanbieters entspricht, der hinzugefügt oder gelöscht werden soll. 
    
8. Rufen Sie die [IMAPITable::FindRow-Methode](imapitable-findrow.md) der Anbietertabelle auf, um die Zeile in der Tabelle zu suchen, die den Zieldienstanbieter darstellt. 
    
9. Rufen [Sie IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md) auf, um den Anbieter hinzuzufügen, oder [IProviderAdmin::D eleteProvider,](iprovideradmin-deleteprovider.md) um ihn aus dem Nachrichtendienst zu entfernen. Übergeben Sie für **CreateProvider** die **PR_DISPLAY_NAME** Eigenschaft des Anbieters als _lpszProvider-Parameter._ Übergeben Sie für beide Methoden die **PR_SERVICE_UID** Eigenschaft des Anbieters als _lpUID-Parameter._ Nachdem der Dienstanbieter hinzugefügt oder gelöscht wurde, wird die Änderung erst angezeigt, nachdem eine neue Sitzung erstellt wurde. 
    
Eine weitere Technik zum Hinzufügen eines Dienstanbieters, insbesondere eines Nachrichtenspeicheranbieters, zu einem Profil umfasst die Erstellung eines Eintragsbezeichners für den Anbieter. Da für die Erstellung eines Eintragsbezeichners Kenntnisse des Formats erforderlich sind, kann diese Technik nur verwendet werden, wenn der Dienstanbieter das Eintragsbezeichnerformat öffentlich gemacht hat. 
  
Mit dem neu erstellten Eintragsbezeichner kann ein Client [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)aufrufen. MAPI erstellt automatisch einen Profilabschnitt im Profil für den Dienstanbieter, fügt ihn jedoch keinem Nachrichtendienst hinzu. 
  
Einige Nachrichtendienste lassen diese Art der dynamischen Änderung nicht zu. Ob sie unterstützt wird, hängt vom Nachrichtendienst ab. Ein weiteres Feature, das möglicherweise unterstützt wird, ist die Möglichkeit, direkt auf die privaten Profilabschnitte eines Nachrichtendiensts zuzugreifen. Wenn der von Ihnen verwendeten Nachrichtendienst diesen Zugriff zulässt, veröffentlicht er die **GUID,** die den privaten Abschnitt in MAPISVC.INF darstellt. Sie können diese **GUID** in einem Aufruf von ["IProviderAdmin::OpenProfileSection"](iprovideradmin-openprofilesection.md) übergeben, um auf den Profilabschnitt zuzugreifen. 
  

