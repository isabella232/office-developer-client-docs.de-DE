---
title: Zugreifen auf Objekte mithilfe der Sitzung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a76397b74642aedf9ad5c9704735d869f61db7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321707"
---
# <a name="accessing-objects-by-using-the-session"></a>Zugreifen auf Objekte mithilfe der Sitzung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Sitzungs Zeiger, den Sie von Ihrem Aufruf an [MAPILogonEx](mapilogonex.md) erhalten, kann für den Zugriff auf eine Vielzahl von Objekten verwendet werden. In der folgenden Tabelle sind die Methoden aufgeführt, die für den Zugriff auf verschiedene Objekte verwendet werden: 
  
|**Objekt**|**Session-Methode**|
|:-----|:-----|
|Profil Abschnitt  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Nachrichtenspeicher  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Adressbuch  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Nachrichtendienst-Verwaltungsobjekt  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Ordner, Nachricht, Adressbuchcontainer, Verteilerliste oder Messagingbenutzer  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Mit der **OpenEntry** -Methode und einer gültigen Eintrags-ID können Sie ein beliebiges Adressbuch-oder Nachrichtenspeicher-Anbieterobjekt öffnen. Es gibt weitere **OpenEntry** -Methoden in MAPI, zusätzlich zur **IMAPISession** -Methode. **OpenEntry** wird in den folgenden Objekten implementiert: 
  
|**Objekt**|**Methode**|
|:-----|:-----|
|Anmeldeobjekt des Adressbuch Anbieters  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Adressbuch  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Adressbuchcontainer  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Sitzung  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Nachrichtenspeicher  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Anmeldeobjekt des Nachrichtenspeicher Anbieters  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Ordner  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Support-Objekt  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Einige **OpenEntry** -Methoden erfordern eine Eintrags-ID des zu öffnenden Objekts, ebenso wie **IMAPISession:: OpenEntry**; andere Methoden lassen die Angabe von NULL zu. Eine NULL-Eintrags-ID wird je nach Objekt unterschiedlich interpretiert. Wenn Sie beispielsweise **IAddrBook:: OpenEntry** mit einer NULL-Eintrags-ID aufrufen, wird der Stammcontainer des Adressbuchs von MAPI geöffnet. Die openEntry- **** Methode des Nachrichtenspeichers verhält sich ähnlich; der Stammordner des Nachrichtenspeichers wird geöffnet. **IMAPIContainer:: OpenEntry**, implementiert von Ordnern und Adressbuch Containern, kann MAPI_E_INVALID_PARAMETER oder den Stammcontainer abhängig von der Implementierung zurückgeben. 
  
Zusätzlich zur Unzulässigkeit eines NULL-Werts für die Eintrags-ID unterscheidet sich die **OpenEntry** -Methode der Sitzung von anderen OpenEntry-Methoden, da ihre Aufgabe nicht das Öffnen von Objekten ist. **** Stattdessen wird die Eintrags-ID untersucht und der Aufruf an eine andere **OpenEntry** -Methode weitergeleitet, die vom entsprechenden Dienstanbieter implementiert wird. Wenn Sie beispielsweise **IMAPISession:: OpenEntry** mit der Eintrags-ID einer Nachricht aufrufen, ruft MAPI die **IMSLogon:: OpenEntry** -Methode des Nachrichtenspeichers auf, der für die Nachricht zuständig ist. 
  
Zusätzlich zur Verwendung der Sitzung zum Öffnen von Objekten verwenden Clients diese, um Sie zu vergleichen. Die [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) -Methode vergleicht Objekte durch Vergleichen Ihrer Eintrags-IDs. Wenn die [MAPIUID](mapiuid.md) -Strukturen, die in den Eintrags-IDs enthalten sind, zum gleichen Dienstanbieter gehören, leitet MAPI den Anruf an diesen Anbieter weiter. **CompareEntryIDs** gibt einen Fehlerwert zurück, wenn die beiden Eintragsbezeichner nicht übereinstimmen. Diese Methode kann zwar Eintragsbezeichner vergleichen, die zu einem beliebigen Objekttyp gehören, **CompareEntryIDs** eignet sich jedoch für Objekte höherer Ebene wie Nachrichtenspeicher und Adressbuchcontainer. Um Objekte mit niedrigerer Ebene zu vergleichen, vergleichen Sie direkt die Suchschlüssel der Objekte (**PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))) oder Record Keys (**PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md))). 
  
Wie **** bei OpenEntry wird **CompareEntryIDs** von mehreren Objekten implementiert. Wählen Sie **** die OpenEntry-und die **CompareEntryID** -Methode entsprechend der Menge der Informationen, die Sie zu den zu öffnenden oder zu vergleichenden Objekten haben. Verwenden Sie die folgenden Richtlinien, wenn Sie entscheiden, welche Schnittstellenmethode aufgerufen werden soll: 
  
- Wenn Sie keine Informationen zu den Zielobjekten haben, rufen Sie [IMAPISession:: OpenEntry](imapisession-openentry.md) oder [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md)auf. Dieser Ansatz ermöglicht den Zugriff auf ein beliebiges Objekt, ist jedoch die langsamste der drei.
    
- Wenn Sie wissen, dass die Zielobjekte Adressbucheinträge und nicht beispielsweise Ordner sind, rufen Sie die [IAddrBook:: OpenEntry](iaddrbook-openentry.md) -oder [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md) -Methode auf. **IAddrBook:: OpenEntry** öffnet den Stammcontainer des Adressbuchs, wenn NULL als Zielobjekt angegeben wird. Dieser Ansatz ermöglicht den Zugriff auf ein beliebiges Adressbuchobjekt und ist schneller als die Verwendung von **IMAPISession**, aber langsamer als die Verwendung von **IMAPIContainer**.
    
- Wenn es sich bei der verwendeten Eintrags-ID um eine kurzfristige Eintrags-ID handelt oder Sie wissen, dass die Zielobjekte zu einem bestimmten Adressbuchcontainer oder-Ordner gehören, rufen Sie die [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) -Methode auf. Dieser Ansatz führt zu einer schnellsten Leistung, ermöglicht jedoch nur den Zugriff auf Objekte in einem bestimmten Container oder Ordner. 
    

