---
title: Erstellen eines Empfängers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e14430d1539b90e089a9dabe1315384050f3dd5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429586"
---
# <a name="creating-a-recipient"></a>Erstellen eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients erstellen Empfänger, wenn sie Nachrichten adressieren und Einträge zu veränderbaren Adressbuchcontainern hinzufügen. MAPI bietet drei Methoden zum Erstellen von Empfängern:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Rufen **Sie IAddrBook::CreateOneOff auf,** wenn Sie Empfänger erstellen, die zum Adressieren von Nachrichten verwendet werden sollen. **CreateOneOff erstellt** einen speziell formatierten one-off-Eintragsbezeichner, der einer Adresse eines bestimmten Adresstyps zugeordnet werden soll. Weitere Informationen zu one-offs und one-off entry identifiers finden Sie unter [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).
  
Rufen **Sie IAddrBook::NewEntry** auf, wenn Sie Empfänger erstellen, die zum Adressieren von Nachrichten oder zum Hinzufügen zu einem Container verwendet werden sollen. **NewEntry verfügt** über drei Parameterpaare, die Eintragsbezeichner enthalten. Diese Parameter werden wie folgt beschrieben: 
  
|**Parameterpaar**|**Beschreibung**|
|:-----|:-----|
| _cbEidContainer_ und  _lpEidContainer_ <br/> |Eintrags-ID für den Container, in den der neue Eintrag platziert werden soll.  <br/> |
| _cbEidNewEntryTpl_ und  _lpEidNewEntryTpl_ <br/> |Eintrags-ID für die Vorlage, die zum Erstellen des neuen Eintrags verwendet werden soll.  <br/> |
| _lpcbEidNewEntry_ und  _lppEidNewEntry_ <br/> |Eintrags-ID für den neuen Eintrag.  <br/> |
   
Um einen Empfänger für eine ausgehende Nachricht zu erstellen, legen Sie  _cbEidContainer_ auf Null und  _lpEidContainer auf_ NULL. **NewEntry** erstellt einen Empfänger mit einer Eintrags-ID, die dem einmalformat entspricht, dem gleichen Empfängertyp, der durch einen Aufruf von **IAddrBook::CreateOneOff** erzeugt wird. 
  
Um einen Empfänger zu erstellen, der in einen bestimmten Container eingefügt werden soll, legen Sie  _lpEidContainer_ auf den Eintragsbezeichner des Containers und  _cbEidContainer_ auf die Anzahl der Bytes im Eintragsbezeichner des Containers. 
  
Um eine Vorlage zum Erstellen eines Empfängers zu verwenden, legen Sie  _lpEidNewEntryTpl_ auf den Eintragsbezeichner der zu verwendenden Vorlage und  _cbEidNewEntryTpl_ auf die Anzahl der Bytes in diesem Eintragsbezeichner. Die meisten veränderbaren Adressbuchcontainer unterstützen eine oder mehrere Vorlagen zum Erstellen von Einträgen eines bestimmten Typs. Bei einmal erstellten Vorlagen handelt es sich in der Regel um Dialogfelder, aber nicht immer. Wenn Sie Informationen in die Vorlage eingeben, wird ein Empfänger mit einer Adresse erzeugt, die für den Typ korrekt formatiert ist. 
  
Rufen Sie die Vorlageneintrags-ID von einer der beiden Abzeichner ab:
  
- Auf **die PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Spalte in der #A0 des Containers zugegriffen wird, indem die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers und **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) als Eigenschaftentag und IID_IMAPITable als Schnittstellenbezeichner angegeben werden. 
    
- Die Eigenschaften **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) eines Adressbuchanbieters, die die Eintragsbezeichner für die Nachrichtenbenutzerobjekt- und Verteilerlistenvorlagen des Anbieters enthalten. 
    
> [!NOTE]
> Verwechseln Sie den Eintragsbezeichner einer neuen Eintragsvorlage nicht mit einem anderen Typ von Eintragsbezeichner, der als Vorlagenbezeichner bezeichnet wird. Eine Vorlagen-ID wird nur von Anbietern verwendet, um Einträge zu verwalten, die von anderen Anbietern kopiert wurden. Es wird nie von Clients verwendet und nicht zum Erstellen neuer Einträge verwendet. 
  
Um dem Benutzer zu ermöglichen, den Typ des zu erstellenden Eintrags zu bestimmen, übergeben Sie null für  _cbEidNewEntryTpl_ und NULL für  _lpEidNewEntryTpl_. In diesem Fall zeigt **NewEntry** ein allgemeines Dialogfeld an, das aus der einmal erstellten TABELLE von MAPI erstellt wurde – eine hierarchische Liste aller Vorlagen, die von jedem Adressbuchanbieter im Profil unterstützt werden. 
  
Wenn ein Adresstyp bestimmt wurde, entweder durch die Einstellung des  _lpEidNewEntryTpl-Parameters_ oder durch eine Auswahl durch den Benutzer aus der Anzeige der einmal verwendeten Tabelle, zeigt **NewEntry** die entsprechende Vorlage mithilfe der Anzeigetabelle an. Alle neuen Eintragsvorlagen unterstützen **die PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft. 
  
Wenn **NewEntry** den Eintragsbezeichner des erstellten Eintrags zurückgeben soll, übergeben Sie eine gültige Adresse für die _Parameter lpcbEidNewEntry_ und _lppEidNewEntry._ MAPI platziert den neuen Eintragsbezeichner an der Adresse, auf die  _von lppEidNewEntry_ verwiesen wird, und die Byteanzahl des neuen Eintragsbezeichners an der Adresse, auf die  _von lpcbEidNewEntry_ verwiesen wird.
  
Rufen [Sie IABContainer::CreateEntry auf,](iabcontainer-createentry.md) um einen Empfänger zu erstellen und ihn in einem bestimmten Adressbuchcontainer zu speichern. Sie können diese Methode nur mit veränderbaren Containern verwenden– Containern, deren AB_MODIFIABLE -Flag in der eigenschaft **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) festgelegt ist. Adressbuchanbieter mit nicht veränderbaren Containern unterstützen diese Methode nicht. Geben Sie den Eintragsbezeichner der Vorlage zum Erstellen eines Eintrags des gewünschten Typs im  _lpEntryID-Parameter_ an. 
  
Geben Sie  _im ulCreateFlags-Parameter_ den Typ der doppelten Eintragsprüfung an, die erforderlich ist, und ob neue Einträge vorhandene einträge ersetzen sollen. Wenn **CreateEntry** aufgrund der doppelten Eintragsüberprüfung, die vom Anbieter auferlegt wurde, kein neues Objekt erstellt werden kann, erwarten Sie nicht, dass ein Fehler oder eine Warnung zurückgegeben wird. Unter diesen Bedingungen geben Anbieter einen Erfolgscode zurück. 
  
Wenn Sie direkt mit einem Container arbeiten und genau wissen, welche Adresstypen der Container erstellen kann, können Sie **IABContainer::CreateEntry** aufrufen und den Eintragsbezeichner für die entsprechende Vorlage übergeben. Der Adressbuchanbieter legt einige anfängliche Standardeigenschaften fest. Sie können **SetProps aufrufen,** um andere zu setzen. Der Benutzer ist nie beteiligt. 
  

