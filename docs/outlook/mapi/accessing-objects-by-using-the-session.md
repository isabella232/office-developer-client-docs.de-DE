---
title: Zugreifen auf Objekte mithilfe der Sitzung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da0ee486979d02f70f24fed2e6e63a5ce5277564
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556980"
---
# <a name="accessing-objects-by-using-the-session"></a>Zugreifen auf Objekte mithilfe der Sitzung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Sitzungszeiger, den Sie von Ihrem Aufruf von [MAPILogonEx](mapilogonex.md) erhalten, kann für den Zugriff auf eine Vielzahl von Objekten verwendet werden. In der folgenden Tabelle sind die Methoden aufgeführt, die für den Zugriff auf verschiedene Objekte verwendet werden: 
  
|**Objekt**|**Session-Methode**|
|:-----|:-----|
|Profilabschnitt  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Nachrichtenspeicher  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Adressbuch  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Nachrichtendienst-Verwaltungsobjekt  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Ordner, Nachricht, Adressbuchcontainer, Verteilerliste oder Messaging-Benutzer  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Mit der **OpenEntry-Methode** und einem gültigen Eintragsbezeichner können Sie ein beliebiges Adressbuch- oder Nachrichtenspeicheranbieterobjekt öffnen. Es gibt weitere **OpenEntry-Methoden** in MAPI, zusätzlich zur **IMAPISession-Methode.** **OpenEntry** ist in den folgenden Objekten implementiert: 
  
|**Objekt**|**Methode**|
|:-----|:-----|
|Anmeldeobjekt des Adressbuchanbieters  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Adressbuch  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Adressbuchcontainer  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Sitzung  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Nachrichtenspeicher  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Anmeldeobjekt des Nachrichtenspeicheranbieters  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Ordner  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Support-Objekt  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Einige **OpenEntry-Methoden** erfordern einen Eintragsbezeichner des Zu öffnenden Objekts, ebenso wie **IMAPISession::OpenEntry**; Andere Methoden ermöglichen das Angeben von NULL. Ein NULL-Eintragsbezeichner wird je nach Objekt unterschiedlich interpretiert. Wenn Sie beispielsweise **IAddrBook::OpenEntry** mit einem NULL-Eintragsbezeichner aufrufen, öffnet MAPI den Stammcontainer des Adressbuchs. Die **OpenEntry-Methode** des Nachrichtenspeichers verhält sich ähnlich. Der Stammordner des Nachrichtenspeichers wird geöffnet. **IMAPIContainer::OpenEntry**, implementiert von Ordnern und Adressbuchcontainern, gibt je nach Implementierer möglicherweise MAPI_E_INVALID_PARAMETER oder den Stammcontainer zurück. 
  
Zusätzlich zum Verbieten eines NULL-Werts für den Eintragsbezeichner unterscheidet sich die **OpenEntry-Methode** der Sitzung von anderen **OpenEntry-Methoden,** da dies nicht das Öffnen von Objekten ist. Stattdessen wird der Eintragsbezeichner untersucht und der Aufruf an eine andere **OpenEntry-Methode** weitergeleitet, die vom entsprechenden Dienstanbieter implementiert wurde. Wenn Sie beispielsweise **IMAPISession::OpenEntry** mit dem Eintragsbezeichner einer Nachricht aufrufen, ruft MAPI die **IMSLogon::OpenEntry-Methode** des Nachrichtenspeichers auf, der für die Nachricht verantwortlich ist. 
  
Zusätzlich zur Verwendung der Sitzung zum Öffnen von Objekten verwenden Clients diese, um sie zu vergleichen. Die [IMAPISession::CompareEntryIDs-Methode](imapisession-compareentryids.md) vergleicht Objekte, indem ihre Eintragsbezeichner verglichen werden. Wenn die in den Eintragsbezeichnern enthaltenen [MAPIUID-Strukturen](mapiuid.md) demselben Dienstanbieter angehören, leitet MAPI den Aufruf an diesen Anbieter weiter. **CompareEntryIDs** gibt einen Fehlerwert zurück, wenn die beiden Eintragsbezeichner nicht übereinstimmen. Obwohl diese Methode Eintragsbezeichner vergleichen kann, die zu einem beliebigen Objekttyp gehören, eignet sich **CompareEntryIDs** am besten für Objekte auf höherer Ebene, z. B. Nachrichtenspeicher und Adressbuchcontainer. Um Objekte der unteren Ebene zu vergleichen, vergleichen Sie direkt die Suchschlüssel der Objekte (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) oder Datensatzschlüssel (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Wie **OpenEntry** wird **CompareEntryIDs** von mehreren Objekten implementiert. Wählen Sie aus, welche **OpenEntry-** und **CompareEntryID-Methode** entsprechend der Menge der Informationen zu dem oder den zu öffnenden oder zu vergleichenden Objekten verwendet werden soll. Verwenden Sie die folgenden Richtlinien, wenn Sie entscheiden, welche Schnittstellenmethode aufgerufen werden soll: 
  
- Wenn Sie keine Informationen zu den Zielobjekten haben, rufen Sie [IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md)auf. Dieser Ansatz ermöglicht den Zugriff auf jedes Objekt, ist aber das langsamste der drei Objekte.
    
- Wenn Sie wissen, dass es sich bei den Zielobjekten nicht um Ordner, sondern um Adressbucheinträge handelt, rufen Sie die [IAddrBook::OpenEntry-](iaddrbook-openentry.md) oder [IAddrBook::CompareEntryIDs-Methode](iaddrbook-compareentryids.md) auf. **IAddrBook::OpenEntry** öffnet den Stammcontainer des Adressbuchs, wenn NULL als Zielobjekt angegeben wird. Dieser Ansatz ermöglicht den Zugriff auf jedes Adressbuchobjekt und ist schneller als die Verwendung von **IMAPISession,** aber langsamer als die Verwendung von **IMAPIContainer**.
    
- Wenn der verwendete Eintragsbezeichner ein kurzfristiger Eintragsbezeichner ist oder Sie wissen, dass die Zielobjekte zu einem bestimmten Adressbuchcontainer oder -ordner gehören, rufen Sie die [IMAPIContainer::OpenEntry-Methode](imapicontainer-openentry.md) auf. Dieser Ansatz liefert die schnellste Leistung, ermöglicht aber nur den Zugriff auf Objekte in einem bestimmten Container oder Ordner. 
    

