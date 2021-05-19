---
title: Zugreifen auf Objekte mithilfe der Sitzung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a76397b74642aedf9ad5c9704735d869f61db7e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410539"
---
# <a name="accessing-objects-by-using-the-session"></a>Zugreifen auf Objekte mithilfe der Sitzung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Sitzungszeiger, den Sie von Ihrem Aufruf von [MAPILogonEx](mapilogonex.md) erhalten, kann für den Zugriff auf eine Vielzahl von Objekten verwendet werden. In der folgenden Tabelle sind die Methoden aufgeführt, die für den Zugriff auf verschiedene Objekte verwendet werden: 
  
|**Objekt**|**Session-Methode**|
|:-----|:-----|
|Abschnitt "Profil"  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Nachrichtenspeicher  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Adressbuch  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Nachrichtendienstverwaltungsobjekt  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Ordner, Nachricht, Adressbuchcontainer, Verteilerliste oder Messagingbenutzer  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Mit der **OpenEntry-Methode** und einem gültigen Eintragsbezeichner können Sie jedes Adressbuch- oder Nachrichtenspeicheranbieterobjekt öffnen. Es gibt weitere **OpenEntry-Methoden** in MAPI, zusätzlich zur **IMAPISession-Methode.** **OpenEntry** wird in den folgenden Objekten implementiert: 
  
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
   
Einige **OpenEntry-Methoden** erfordern einen Eintragsbezeichner des zu öffnenden Objekts, ebenso **IMAPISession::OpenEntry**; Andere Methoden ermöglichen die Angabe von NULL. Ein NULL-Eintragsbezeichner wird je nach Objekt unterschiedlich interpretiert. Wenn Sie beispielsweise **IAddrBook::OpenEntry** mit einem NULL-Eintragsbezeichner aufrufen, öffnet MAPI den Stammcontainer des Adressbuchs. Die **OpenEntry-Methode** des Nachrichtenspeichers verhält sich ähnlich. Der Stammordner des Nachrichtenspeichers wird geöffnet. **IMAPIContainer::OpenEntry**, das von Ordnern und Adressbuchcontainern implementiert wird, gibt je nach Implementer möglicherweise MAPI_E_INVALID_PARAMETER oder den Stammcontainer zurück. 
  
Die **OpenEntry-Methode** der Sitzung unterscheidet sich nicht nur vom Zulassen eines NULL-Werts für die Eintrags-ID, sondern auch von anderen **OpenEntry-Methoden,** da es sich nicht um das Öffnen von Objekten handelt. Stattdessen wird die Eintrags-ID untersucht und der Aufruf an eine andere **OpenEntry-Methode** weitergeleitet, die vom entsprechenden Dienstanbieter implementiert wurde. Wenn Sie beispielsweise **IMAPISession::OpenEntry** mit dem Eintragsbezeichner einer Nachricht aufrufen, ruft MAPI die **IMSLogon::OpenEntry-Methode** des Nachrichtenspeichers auf, der für die Nachricht zuständig ist. 
  
Zusätzlich zur Verwendung der Sitzung zum Öffnen von Objekten verwenden Clients sie, um sie zu vergleichen. Die [IMAPISession::CompareEntryIDs-Methode](imapisession-compareentryids.md) vergleicht Objekte durch Vergleichen ihrer Eintragsbezeichner. Wenn die in den Eintragsbezeichnern enthaltenen [MAPIUID-Strukturen](mapiuid.md) demselben Dienstanbieter angehören, wird der Aufruf von MAPI an diesen Anbieter weitergeleitet. **CompareEntryIDs** gibt einen Fehlerwert zurück, wenn die beiden Eintragsbezeichner nicht übereinstimmen. Obwohl diese Methode Eintragsbezeichner vergleichen kann, die zu einem beliebigen Objekttyp gehören, funktioniert **CompareEntryIDs** am besten für Objekte höherer Ebene wie Nachrichtenspeicher und Adressbuchcontainer. Zum Vergleichen von Objekten auf niedrigerer Ebene vergleichen Sie direkt die Suchtasten der Objekte (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) oder Datensatzschlüssel (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
**CompareEntryIDs** wird wie **OpenEntry** von mehreren Objekten implementiert. Wählen Sie **die OpenEntry-** und **CompareEntryID-Methode** entsprechend der Menge an Informationen, die Sie über das zu öffnende oder zu vergleichende Objekt oder die objekte verfügen. Verwenden Sie die folgenden Richtlinien, wenn Sie entscheiden, welche Schnittstellenmethode sie aufrufen soll: 
  
- Wenn Sie keine Informationen zu den Zielobjekten haben, rufen Sie [IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMAPISession::CompareEntryIDs auf.](imapisession-compareentryids.md) Dieser Ansatz ermöglicht den Zugriff auf jedes Objekt, ist jedoch das langsamste der drei.
    
- Wenn Sie wissen, dass es sich bei den Zielobjekten um Adressbucheinträge und nicht beispielsweise um Ordner handelt, rufen Sie die [IAddrBook::OpenEntry-](iaddrbook-openentry.md) oder [IAddrBook::CompareEntryIDs-Methode](iaddrbook-compareentryids.md) auf. **IAddrBook::OpenEntry** öffnet den Stammcontainer des Adressbuchs, wenn NULL als Zielobjekt angegeben wird. Dieser Ansatz ermöglicht den Zugriff auf jedes Adressbuchobjekt und ist schneller als die Verwendung von **IMAPISession,** aber langsamer als die Verwendung von **IMAPIContainer**.
    
- Wenn es sich bei der verwendeten Eintrags-ID um eine kurzfristige Eintrags-ID handelt oder Wenn Sie wissen, dass die Zielobjekte zu einem bestimmten Adressbuchcontainer oder -ordner gehören, rufen Sie die [IMAPIContainer::OpenEntry-Methode](imapicontainer-openentry.md) auf. Dieser Ansatz bietet die schnellste Leistung, ermöglicht jedoch nur den Zugriff auf Objekte in einem bestimmten Container oder Ordner. 
    

