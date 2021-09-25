---
title: Erstellen eines Empfängers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5f09dfbdc22690e20a568dedd9974a9b6633505c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588217"
---
# <a name="creating-a-recipient"></a>Erstellen eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients erstellen Empfänger, wenn sie Nachrichten adressieren und Einträge zu modifizierbaren Adressbuchcontainern hinzufügen. MAPI bietet drei Methoden zum Erstellen von Empfängern:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Rufen Sie **IAddrBook::CreateOneOff** auf, wenn Sie Empfänger zum Adressieren von Nachrichten erstellen. **CreateOneOff** erstellt einen speziell formatierten einmaligen Eintragsbezeichner, der einer Adresse eines bestimmten Adresstyps zugeordnet wird. Weitere Informationen zu einmaligen und einmaligen Eintragsbezeichnern finden Sie unter ["One-Off Addresses"](one-off-addresses.md) und ["One-Off Entry Identifiers".](one-off-entry-identifiers.md)
  
Rufen Sie **IAddrBook auf::NewEntry,** wenn Sie Empfänger erstellen, die entweder zum Adressieren von Nachrichten oder zum Hinzufügen zu einem Container verwendet werden sollen. **NewEntry** verfügt über drei Parameterpaare, die Eintragsbezeichner enthalten. Diese Parameter werden wie folgt beschrieben: 
  
|**Parameterpaar**|**Beschreibung**|
|:-----|:-----|
| _cbEidContainer_ und  _lpEidContainer_ <br/> |Eintragsbezeichner für den Container, in dem der neue Eintrag platziert werden soll.  <br/> |
| _cbEidNewEntryTpl_ und  _lpEidNewEntryTpl_ <br/> |Eintragsbezeichner für die Vorlage, die zum Erstellen des neuen Eintrags verwendet werden soll.  <br/> |
| _lpcbEidNewEntry_ und  _lppEidNewEntry_ <br/> |Eintragsbezeichner für den neuen Eintrag.  <br/> |
   
Um einen Empfänger für eine ausgehende Nachricht zu erstellen, legen Sie  _cbEidContainer_ auf Null und  _lpEidContainer_ auf NULL fest. **NewEntry** erstellt einen Empfänger mit einem Eintragsbezeichner, der dem einmaligen Format entspricht, dem gleichen Empfängertyp, der durch einen Aufruf von **IAddrBook erzeugt wird::CreateOneOff**. 
  
Um einen Empfänger zu erstellen, der in einen bestimmten Container eingefügt werden soll, legen Sie  _"lpEidContainer"_ auf den Eintragsbezeichner des Containers und  _"cbEidContainer"_ auf die Anzahl der Bytes im Eintragsbezeichner des Containers fest. 
  
Um eine Vorlage zum Erstellen eines Empfängers zu verwenden, legen Sie  _lpEidNewEntryTpl_ auf den Eintragsbezeichner der zu verwendenden Vorlage und  _cbEidNewEntryTpl_ auf die Anzahl der Bytes in diesem Eintragsbezeichner fest. Die meisten modifizierbaren Adressbuchcontainer unterstützen eine oder mehrere Vorlagen zum Erstellen von Einträgen eines bestimmten Typs. Einmalige Vorlagen sind in der Regel, aber nicht immer, Dialogfelder. Das Eingeben von Informationen in die Vorlage erzeugt einen Empfänger mit einer Adresse, die für den Typ richtig formatiert ist. 
  
Abrufen des Vorlageneintragsbezeichners aus den beiden:
  
- Die **Spalte PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) in der einmaligen Tabelle des Containers, auf die zugegriffen wird, indem die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers aufgerufen und **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) als Eigenschaftentag und IID_IMAPITable als Schnittstellenbezeichner angegeben werden. 
    
- Die **Eigenschaften PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) eines Adressbuchanbieters, die die Eintragsbezeichner für das Messagingbenutzerobjekt und Die Verteilerlistenvorlagen des Anbieters enthalten. 
    
> [!NOTE]
> Verwechseln Sie den Eintragsbezeichner einer neuen Eintragsvorlage nicht mit einem anderen Eintragsbezeichnertyp, der als Vorlagenbezeichner bezeichnet wird. Ein Vorlagenbezeichner wird nur von Anbietern zum Verwalten von Einträgen verwendet, die von anderen Anbietern kopiert wurden. Es wird nie von Clients verwendet und nicht zum Erstellen neuer Einträge verwendet. 
  
Damit der Benutzer den Typ des zu erstellenden Eintrags ermitteln kann, übergeben Sie null für _cbEidNewEntryTpl_ und NULL für _lpEidNewEntryTpl._ In diesem Fall zeigt **NewEntry** ein allgemeines Dialogfeld an, das aus der einmaligen MapI-Tabelle erstellt wurde – eine hierarchische Liste aller Vorlagen, die von jedem Adressbuchanbieter im Profil unterstützt werden. 
  
Wenn ein Adresstyp bestimmt wurde, entweder durch die Einstellung des  _parameters lpEidNewEntryTpl_ oder eine Auswahl durch den Benutzer aus der Einmaligen Tabellenanzeige, zeigt **NewEntry** die entsprechende Vorlage mithilfe der Anzeigetabelle an. Alle neuen Eintragsvorlagen unterstützen die **Eigenschaft PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). 
  
Damit **NewEntry** den Eintragsbezeichner des erstellten Eintrags zurückgibt, übergeben Sie eine gültige Adresse für die Parameter _lpcbEidNewEntry_ und _lppEidNewEntry._ MAPI platziert den neuen Eintragsbezeichner an der Adresse, auf die durch  _lppEidNewEntry_ verwiesen wird, und die Byteanzahl des neuen Eintragsbezeichners an der Adresse, auf die von  _lpcbEidNewEntry_ verwiesen wird.
  
Rufen Sie [IABContainer::CreateEntry](iabcontainer-createentry.md) auf, um einen Empfänger zu erstellen und in einem bestimmten Adressbuchcontainer zu speichern. Sie können diese Methode nur mit modifizierbaren Containern verwenden– Containern, deren **AB_MODIFIABLE-Flag** in der PR_CONTAINER_FLAGS -Eigenschaft ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) festgelegt ist. Adressbuchanbieter mit nichtmodifiierbaren Containern unterstützen diese Methode nicht. Geben Sie den Eintragsbezeichner der Vorlage zum Erstellen eines Eintrags des gewünschten Typs im  _LpEntryID-Parameter_ an. 
  
Geben Sie im  _Parameter ulCreateFlags_ den Typ der erforderlichen Duplikateintragsprüfung an und geben Sie an, ob vorhandene Einträge durch neue Einträge ersetzt werden sollen. Wenn **CreateEntry** aufgrund der doppelten Eintragsprüfung durch den Anbieter kein neues Objekt erstellen kann, wird kein Fehler oder eine Warnung zurückgegeben. Unter diesen Bedingungen geben Anbieter einen Erfolgscode zurück. 
  
Wenn Sie direkt mit einem Container arbeiten und genau wissen, welche Adressentypen der Container erstellen kann, können Sie **IABContainer::CreateEntry** aufrufen und den Eintragsbezeichner für die entsprechende Vorlage übergeben. Der Adressbuchanbieter legt einige anfängliche Standardeigenschaften fest. Sie können **SetProps** aufrufen, um andere festzulegen. Der Benutzer ist nie beteiligt. 
  

