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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329561"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwenden Sie die [IProviderAdmin: IUnknown](iprovideradminiunknown.md) -schnittStelle, um Dienstanbieter in einem Nachrichtendienst hinzuzufügen oder zu löschen. Sie können einen **IProviderAdmin** -Zeiger abrufen, indem Sie [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md)aufrufen. In der Anbieter Tabelle, die über [IProviderAdmin::](iprovideradmin-getprovidertable.md)getproviderable zugänglich ist, werden Informationen zu den Dienstanbietern aufgelistet, die derzeit im Nachrichtendienst installiert sind. Clients und Dienstanbieter können die Provider-Tabelle verwenden, um auf den Namen der Anbieter-DLL-Datei zuzugreifen, beispielsweise auf die **MAPIUID**, den Anzeigenamen und den Typ des Anbieters sowie auf Informationen zum Nachrichtendienst. Weitere Informationen finden Sie unter [Provider Tables](provider-tables.md).
  
 **So können Sie einen Dienstanbieter in einem Nachrichtendienst hinzufügen oder löschen**
  
1. Rufen Sie die **AdminServices** -Methode auf, um auf ein Nachrichtendienst-Verwaltungsobjekt zuzugreifen. 
    
2. Rufen Sie [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) auf, um auf die Nachrichtendienst Tabelle zuzugreifen. 
    
3. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_SERVICE_NAME** ([pidtagservicename (](pidtagservicename-canonical-property.md)) mit dem Namen des zu verwendenden Nachrichtendiensts entspricht. geändert. 
    
4. Rufen Sie die [IMAPITable:: FindRow](imapitable-findrow.md) -Methode der Nachrichtendienst Tabelle auf, um die Zeile in der Tabelle zu suchen, die den Ziel Nachrichtendienst darstellt. 
    
5. Rufen Sie [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md) auf, um einen **IProviderAdmin** -Zeiger abzurufen. Übergeben Sie die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Spalte aus der Zeile Nachrichtendienst als _lpUID_ -Parameter. 
    
6. Rufen Sie [IProviderAdmin::](iprovideradmin-getprovidertable.md) getproviderable auf, um auf die Anbieter Tabelle zuzugreifen. 
    
7. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer SPropertyRestriction-Struktur, die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_PROVIDER_DISPLAY** ([pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md)) mit dem Namen des zu verwendenden Dienstanbieters entspricht. hinzugefügt oder gelöscht. 
    
8. Rufen Sie die [IMAPITable:: FindRow](imapitable-findrow.md) -Methode der Anbieter Tabelle auf, um die Zeile in der Tabelle zu suchen, die den Zielanbieter darstellt. 
    
9. Rufen Sie [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md) auf, um den Anbieter oder [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md) hinzuzufügen, um Sie aus dem Nachrichtendienst zu entfernen. Übergeben **** Sie für CreateProvider die **PR_DISPLAY_NAME** -Eigenschaft des Anbieters als _lpszProvider_ -Parameter. Übergeben Sie für beide Methoden die **PR_SERVICE_UID** -Eigenschaft des Anbieters als _lpUID_ -Parameter. Nachdem der Dienstanbieter hinzugefügt oder gelöscht wurde, wird die Änderung erst dann sichtbar, wenn eine neue Sitzung erstellt wird. 
    
Eine weitere Methode zum Hinzufügen eines Dienstanbieters, insbesondere eines Nachrichtenspeicher Anbieters, zu einem Profil besteht darin, eine Eintrags-ID für den Anbieter zu erstellen. Da das Erstellen eines Eintrags Bezeichners Kenntnisse des Formats erfordert, kann diese Technik nur verwendet werden, wenn der Dienstanbieter sein Eintrags-ID-Format öffentlich gemacht hat. 
  
Mit der neu erstellten Eintrags-ID kann ein Client [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md)aufrufen. MAPI erstellt automatisch einen Profil Abschnitt im Profil des Dienstanbieters, fügt ihn jedoch nicht zu einem Nachrichtendienst hinzu. 
  
Bei einigen Nachrichtendiensten ist diese Art der dynamischen Änderung nicht zulässig. ob Sie unterstützt wird, ist der Nachrichtendienst. Ein weiteres Feature, das möglicherweise nicht unterstützt wird, ist die Möglichkeit, direkt auf private Profilabschnitte eines Nachrichtendiensts zuzugreifen. Wenn der von Ihnen verwendete Nachrichtendienst diesen Zugriff zulässt, wird die **GUID** veröffentlicht, die den privaten Abschnitt in MAPISVC. inf darstellt. Sie können diese **GUID** in einem Aufruf von [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) für den Zugriff auf den Profil Abschnitt weiterleiten. 
  

