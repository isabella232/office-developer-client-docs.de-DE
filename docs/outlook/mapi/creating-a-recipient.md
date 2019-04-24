---
title: Erstellen eines Empfängers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e14430d1539b90e089a9dabe1315384050f3dd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332956"
---
# <a name="creating-a-recipient"></a>Erstellen eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients erstellen Empfänger, wenn Sie Nachrichten adressieren und Einträge zu änderbaren Adressbuch Containern hinzufügen. MAPI bietet drei Methoden zum Erstellen von Empfängern:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Rufen Sie **IAddrBook:: CreateOneOff** auf, wenn Sie Empfänger zum Adressieren von Nachrichten erstellen. **CreateOneOff** erstellt eine speziell formatierte einmalige Eintrags-ID, die einer Adresse eines bestimmten Adresstyps zugeordnet werden soll. Weitere Informationen zu einmaligen und einmaligen Eintrags Bezeichnern finden Sie unter [einmalige Adressen](one-off-addresses.md) und [einmalige Eintrags-IDs](one-off-entry-identifiers.md).
  
Rufen Sie **IAddrBook:: neuer Eintrag** auf, wenn Sie Empfänger erstellen, die zum Adressieren von Nachrichten oder zum Hinzufügen zu einem Container verwendet werden sollen. **** Der Neueintrag hat drei Parameter Paare, die Eintrags-IDs enthalten. Diese Parameter werden wie folgt beschrieben: 
  
|**Parameter paar**|**Beschreibung**|
|:-----|:-----|
| _cbEidContainer_ und _lpEidContainer_ <br/> |Eintrags-ID für den Container, in den der neue Eintrag eingefügt werden soll.  <br/> |
| _cbEidNewEntryTpl_ und _lpEidNewEntryTpl_ <br/> |Eintrags-ID für die Vorlage, die zum Erstellen des neuen Eintrags verwendet werden soll.  <br/> |
| _lpcbEidNewEntry_ und _lppEidNewEntry_ <br/> |Eintrags-ID für den neuen Eintrag.  <br/> |
   
Um einen Empfänger für eine ausgehende Nachricht zu erstellen, legen Sie _cbEidContainer_ auf NULL und _lpEidContainer_ auf NULL fest. **** Der Neueintrag erstellt einen Empfänger mit einer Eintrags-ID, die dem einmaligen Format entspricht, dem gleichen Empfängertyp, der durch einen Aufruf von **IAddrBook:: CreateOneOff**. 
  
Zum Erstellen eines Empfängers, der in einen bestimmten Container eingefügt werden soll, legen Sie _lpEidContainer_ auf die Eintrags-ID des Containers und _cbEidContainer_ auf die Anzahl der Bytes in der Eintrags-ID des Containers fest. 
  
Wenn Sie eine Vorlage zum Erstellen eines Empfängers verwenden möchten, legen Sie _lpEidNewEntryTpl_ auf den Eintragsbezeichner der Vorlage fest, die verwendet werden soll, und _cbEidNewEntryTpl_ auf die Anzahl von Bytes in dieser Eintrags-ID. Die meisten änderbaren Adressbuchcontainer unterstützen eine oder mehrere Vorlagen zum Erstellen von Einträgen eines bestimmten Typs. Einmalige Vorlagen sind in der Regel, jedoch nicht immer, Dialogfelder. Durch das Eingeben von Informationen in die Vorlage wird ein Empfänger mit einer Adresse erstellt, die für den Typ ordnungsgemäß formatiert ist. 
  
Rufen Sie den Vorlagen Eintragsbezeichner aus dem folgenden aus:
  
- Die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Spalte in der einmaligen Tabelle des Containers, auf die durch Aufrufen der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers zugegriffen wird und **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md)) als das Property-Tag und die IID_IMAPITable als Schnittstellenbezeichner. 
    
- Die Eigenschaften **PR_DEF_CREATE_MAILUSER** ([Pidtagdefcreatemailuser (](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([pidtagdefcreatedl (](pidtagdefcreatedl-canonical-property.md)) eines Adressbuch Anbieters enthalten die Eintragsbezeichner für das Messaging-Benutzerobjekt des Anbieters und Verteilerlisten Vorlagen. 
    
> [!NOTE]
> Verwechseln Sie die Eintrags-ID einer neuen Eintrags Vorlage nicht mit einem anderen Typ von Eintrags-ID als Vorlagenbezeichner. Ein Vorlagenbezeichner wird nur von Anbietern verwendet, um Einträge zu verwalten, die von anderen Anbietern kopiert wurden. Sie wird nie von Clients verwendet und nicht zum Erstellen neuer Einträge verwendet. 
  
Um dem Benutzer zu ermöglichen, den Typ des zu erstellenden Eintrags zu bestimmen, geben Sie NULL für _cbEidNewEntryTpl_ und NULL für _lpEidNewEntryTpl_. Wenn dies der Fall ist, zeigt der **Eintrag** ein allgemeines Dialogfeld aus der EINMALIGEn MAPI-Tabelle an, eine hierarchische Liste aller Vorlagen, die von jedem Adressbuchanbieter im Profil unterstützt werden. 
  
Wenn ein Adresstyp ermittelt wurde, entweder durch die Einstellung des _lpEidNewEntryTpl_ -Parameters oder durch eine Auswahl des Benutzers aus der einmaligen Tabellenanzeige, zeigt der **Eintrag** die entsprechende Vorlage mithilfe der Anzeigetabelle an. Alle neuen Eintrags Vorlagen unterstützen die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft. 
  
Um den **** Eintragsbezeichner des erstellten Eintrags zurückzugeben, übergeben Sie eine gültige Adresse für die Parameter _lpcbEidNewEntry_ und _lppEidNewEntry_ . MAPI platziert die neue Eintrags-ID an der Adresse, auf die _lppEidNewEntry_ , und die Bytezahl der neuen Eintrags-ID an der Adresse, auf die von _lpcbEidNewEntry_verwiesen wird.
  
Rufen Sie [IABContainer:: CreateEntry](iabcontainer-createentry.md) auf, um einen Empfänger zu erstellen und ihn in einem bestimmten Adressbuchcontainer zu speichern. Sie können diese Methode nur mit änderbaren Containern verwenden – Container, für die das AB_MODIFIABLE-Flag in der **PR_CONTAINER_FLAGS** ([pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))-Eigenschaft festgelegt ist. Adressbuchanbieter mit nicht änderbaren Containern unterstützen diese Methode nicht. Geben Sie den Eintragsbezeichner der Vorlage zum Erstellen eines Eintrags des gewünschten Typs im Parameter _lpEntryID_ an. 
  
Geben Sie im _ulCreateFlags_ -Parameter den Typ der erforderlichen doppelten Eingabeüberprüfung an und ob neue Einträge vorhandene ersetzen sollen. Wenn **CreateEntry** aufgrund der doppelten Überprüfung durch den Anbieter kein neues Objekt erstellt, erwarten Sie nicht, dass ein Fehler oder eine Warnung zurückgegeben wird. Unter diesen Bedingungen gibt der Anbieter einen Erfolgscode zurück. 
  
Wenn Sie direkt mit einem Container arbeiten und genau wissen, welche Adresstypen der Container erstellen kann, können Sie **IABContainer:: CreateEntry** aufrufen und die Eintrags-ID für die entsprechende Vorlage weitergeben. Der Adressbuchanbieter legt einige anfängliche Standardeigenschaften fest; Sie können setProps aufrufen, um andere festzulegen. **** Der Benutzer ist nie beteiligt. 
  

