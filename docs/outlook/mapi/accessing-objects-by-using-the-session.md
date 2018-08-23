---
title: Zugreifen auf Objekte durch eine Sitzung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f0696ad4d15274e4af18d2246dd124c1bfee1a2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589406"
---
# <a name="accessing-objects-by-using-the-session"></a>Zugreifen auf Objekte durch eine Sitzung

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Der Sitzung Zeiger, den Sie aus den Anruf auf [MAPILogonEx](mapilogonex.md) erhalten kann verwendet werden, um eine Vielzahl von Objekten zuzugreifen. Die folgende Tabelle enthält die Methoden, die verwendet werden, um verschiedene Objekte zuzugreifen: 
  
|**Objekt**|**Session-Methode**|
|:-----|:-----|
|Profilabschnitt  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Nachrichtenspeicher  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Adressbuch  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objekt "Message" Service-Verwaltung  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Ordner, Nachricht, Adressbuchcontainer, Verteilerliste oder messaging-Benutzer  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Mit der Methode **OpenEntry** und eine gültige Eintrags-ID können Sie alle Address Book oder einer Nachricht Store Anbieter-Objekt öffnen. Es sind andere Methoden **OpenEntry** in MAPI, zusätzlich zu der **IMAPISession** -Methode. **OpenEntry** wird in den folgenden Objekten implementiert: 
  
|**Objekt**|**Methode**|
|:-----|:-----|
|--Adressbuchanbieter Anmeldung-Objekt  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Adressbuch  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Adressbuchcontainer  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Sitzung  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Nachrichtenspeicher  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Nachricht-Speicheranbieter Anmeldung-Objekt  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Ordner  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Support-Objekt  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Einige Methoden **OpenEntry** erforderlich einen Eintrag Bezeichner des Objekts geöffnet werden, **IMAPISession::OpenEntry**. andere Methoden ermöglichen NULL angegeben werden. Eine NULL-Eintrags-ID wird je nach dem Objekt unterschiedlich interpretiert. Wenn Sie einen NULL-Eintrags-ID **IAddrBook::OpenEntry** aufrufen, wird MAPI beispielsweise den Stammcontainer des Adressbuchs geöffnet. Der Nachrichtenspeicher **OpenEntry** -Methode verhält sich wie; Es wird im Stammordner des Nachrichtenspeichers geöffnet. **IMAPIContainer::OpenEntry**, von Ordnern und Address Book-Containern und implementiert möglicherweise MAPI_E_INVALID_PARAMETER oder die Stammcontainer, je nach der Implementierung zurück. 
  
Zusätzlich zum Ablehnen von eines NULL-Werts für die Eintrags-ID, unterscheidet sich die Sitzung **OpenEntry** -Methode von anderen Methoden **OpenEntry** , da ihre Arbeit ist nicht für Objekte zu öffnen. Stattdessen untersucht die Eintrags-ID, und leitet den Anruf an eine andere **OpenEntry** -Methode, die von den entsprechenden Dienstanbieter implementiert wird. Angenommen, wenn Sie mit der Eintrags-ID einer Nachricht **IMAPISession::OpenEntry** aufrufen, ruft MAPI die **IMSLogon::OpenEntry** -Methode des Nachrichtenspeichers verantwortlich für die Nachricht. 
  
Zusätzlich zur Verwendung der Sitzung auf um Objekte zu öffnen, verwenden sie Clients um zu vergleichen. Die [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) -Methode vergleicht Objekte, indem ihre Eintragsbezeichner vergleichen. Wenn die [MAPIUID](mapiuid.md) Strukturen innerhalb der Eintragsbezeichner mit der gleichen Dienstanbieter gehören, leitet MAPI den Anruf an diesen Anbieter. **CompareEntryIDs** gibt einen Fehlerwert zurück, wenn die zwei-Eintragsbezeichner nicht übereinstimmen. Obwohl diese Methode Eintragsbezeichner, die für jede Art von Objekt gehören vergleichen kann, die besten Ergebnisse **CompareEntryIDs** für übergeordnete Objekte wie Nachrichtenspeicher und Address Book Container. Zum Vergleichen von untergeordneten Objekte vergleichen Sie direkt, die für die Objekte Search (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) oder aufzeichnen Schlüssel (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
**CompareEntryIDs** wird durch mehrere Objekte wie **OpenEntry**implementiert. Wählen Sie die **OpenEntry** und **CompareEntryID** Methode geöffnet oder verglichen werden entsprechend den Umfang der Informationen, die Ihnen zu einem oder mehreren Objekten verwenden. Verwenden Sie bei der Entscheidung, welche Schnittstellenmethode aufrufen, die folgenden Richtlinien: 
  
- Wenn Sie keine Informationen über die Zielobjekte haben, rufen Sie [IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Dieser Ansatz ermöglicht den Zugriff auf ein beliebiges Objekt, jedoch ist der langsamste der drei.
    
- Wenn Sie wissen, dass die Zielobjekte Adressbucheinträge statt, beispielsweise Ordner sind, rufen Sie die [IAddrBook::OpenEntry](iaddrbook-openentry.md) oder [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) -Methode. **IAddrBook::OpenEntry** öffnet den Stammcontainer des Adressbuchs, wenn NULL als Zielobjekt angegeben ist. Dieser Ansatz ermöglicht den Zugriff auf ein beliebiges Address Book-Objekt und schneller als die Verwendung von **IMAPISession**, aber langsamer als die Verwendung von **IMAPIContainer**ist.
    
- Rufen Sie Wenn die Eintrags-ID verwendeten kurzfristige Eintrags-ID ist oder wenn Sie wissen, dass die Zielobjekte in einer bestimmten Adressbuchcontainer oder einen Ordner gehören, die [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) -Methode. Dieser Ansatz ergibt sich die schnellste Leistung, aber nur für Objekte in einem bestimmten Container oder Ordner Zugriff wird aktiviert. 
    

