---
title: Hinzufügen oder Löschen von Anbietern in einem Message-Dienst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 05d6d548032476062127f21b23aa2ce141ed1b65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791266"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Hinzufügen oder Löschen von Anbietern in einem Message-Dienst

  
  
**Betrifft**: Outlook 
  
Verwenden Sie zum Hinzufügen oder löschen-Dienstanbieter in einem Message-Dienst, der [IProviderAdmin: IUnknown](iprovideradminiunknown.md) Schnittstelle. Sie können einen Zeiger **IProviderAdmin** durch Aufrufen von [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)abrufen. Die Anbieter-Tabelle, die über [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), zugegriffen werden enthält Informationen zu den Dienstanbieter, die derzeit in der Nachrichtendienst installiert. Clients und -Dienstanbieter können die Provider-Tabelle verwenden, um Zugriff auf den Namen der Anbieter DLL-Datei, z. B. oder **MAPIUID**, Anzeigename und Typ der Anbieter sowie Informationen zu den Dienst. Weitere Informationen finden Sie unter [Provider Tabellen](provider-tables.md).
  
 **Hinzufügen oder Löschen von einem Dienstanbieter in einem Message-Dienst**
  
1. Rufen Sie die **AdminServices** -Methode, um eine Nachricht Service Administration-Objekt zuzugreifen. 
    
2. Rufen Sie [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) die Tabelle der Dienste für den Zugriff auf. 
    
3. Erstellen Sie eine eigenschaftseinschränkung mit einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) entspricht mit dem Namen des Diensts Nachricht sein geändert. 
    
4. Rufen Sie die Nachricht Service-Tabelle [IMAPITable](imapitable-findrow.md) -Methode, um die Zeile in der Tabelle zu finden, die die gezielte Messagingdiensts darstellt. 
    
5. Rufen Sie [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) , um einen Zeiger **IProviderAdmin** abzurufen. Übergeben Sie die Spalte **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) aus der Nachricht Service Tabellenzeile als _LpUID_ -Parameter. 
    
6. Rufen Sie [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) Zugriff auf die Anbieter-Tabelle. 
    
7. Erstellen Sie eine eigenschaftseinschränkung verwendet eine SPropertyRestriction-Struktur, die ermittelt **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) mit dem Namen des Dienstanbieters, werden soll hinzugefügt oder gelöscht. 
    
8. Rufen Sie die Anbieter-Tabelle [IMAPITable](imapitable-findrow.md) -Methode, um die Zeile in der Tabelle zu finden, die den vorgesehenen Dienstanbieter darstellt. 
    
9. Rufen Sie [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md) den Anbieter hinzugefügt oder [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md) , um es aus dem Nachrichtendienst zu entfernen. **CreateProvider**des Anbieters **PR_DISPLAY_NAME** -Eigenschaft als _LpszProvider_ -Parameter übergeben. Eine der Methoden übergeben Sie des Anbieters **PR_SERVICE_UID** -Eigenschaft als _LpUID_ -Parameter. Nachdem der Dienstanbieter hinzugefügt oder gelöscht wurde, wird die Änderung nicht offensichtlich, bis eine neue Sitzung erstellt wird. 
    
Eine andere Methode zum Hinzufügen von einem Dienstanbieter, insbesondere einer Nachricht Anbieter zu einem Profil umfasst eine Eintrags-ID für den Anbieter erstellen. Da beim Erstellen eines Eintrags-ID des Formats Knowledge erfordert, kann dieses Verfahren nur verwendet werden, wenn der Dienstanbieter seinem Eintrags-ID-Format veröffentlicht hat. 
  
Mit der neu erstellten Eintrags-ID kann ein Client [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)aufrufen. MAPI automatisch ein Profilabschnitt in das Profil für den Dienstanbieter erstellt, aber nicht mit einem Nachrichtendienst hinzu. 
  
Diese Art von dynamischen Änderung zulassen einige Nachrichtendienste nicht; Message-Dienst ist unabhängig davon, ob es unterstützt wird. Ein weiteres Feature, die möglicherweise nicht unterstützt ist die Möglichkeit, eine Messagingdiensts private Profil Abschnitten direkt zugreifen. Wenn der Nachrichtendienst, den Sie verwenden diesen Zugriff zulässt, wird es die **GUID** veröffentlichen, die den privaten Abschnitt in MAPISVC.INF darstellt. Sie können einen Anruf an [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) Profilabschnitt Zugriff auf diese **GUID** übergeben. 
  

