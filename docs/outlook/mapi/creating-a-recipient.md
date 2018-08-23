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
ms.openlocfilehash: 4d4777077dae5effed9f233dd020628ee0dcfed5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578045"
---
# <a name="creating-a-recipient"></a>Erstellen eines Empfängers

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Clients erstellen Empfänger an, wenn sie Nachrichten Adressierung sind und beim Hinzufügen von Einträgen änderbare Address Book Containern. MAPI bietet drei Methoden für das Erstellen von Empfängern:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Rufen Sie **IAddrBook::CreateOneOff** beim Erstellen von Empfängern verwendet werden, um Nachrichten adressieren. **CreateOneOff** erstellt einen Bezeichner speziell formatierten Eingangs eine Adresse für einen bestimmten Adresstyp zugeordnet werden soll. Weitere Informationen zu Fly und einmaligen-Eintragsbezeichner finden Sie unter [Einmal-Adressen](one-off-addresses.md) und [Einmaligen-Eintragsbezeichner](one-off-entry-identifiers.md).
  
Anruf **IAddrBook::NewEntry** beim Erstellen der Empfänger werden verwendet, entweder zum Adressieren von Nachrichten oder um einen Container hinzuzufügen. **NewEntry** hat drei Parameter, die Eintragsbezeichner enthalten-Paare. Diese Parameter sind wie folgt beschrieben: 
  
|**Parameterpaar**|**Beschreibung**|
|:-----|:-----|
| _CbEidContainer_ und _lpEidContainer_ <br/> |Entry-ID für den Container, in dem der neue Eintrag platziert werden soll.  <br/> |
| _CbEidNewEntryTpl_ und _lpEidNewEntryTpl_ <br/> |Entry-ID für die Vorlage verwendet werden, um den neuen Eintrag erstellen.  <br/> |
| _LpcbEidNewEntry_ und _lppEidNewEntry_ <br/> |Entry-ID für den neuen Eintrag.  <br/> |
   
Um einen Empfänger für eine ausgehende Nachricht zu erstellen, legen Sie _CbEidContainer_ auf 0 (null) und _LpEidContainer_ auf NULL fest. **NewEntry** erstellt einen Empfänger mit einem Eintrag Bezeichner, der dem einmaligen Format, den gleichen Typ des Empfängers entspricht, die durch einen Aufruf von **IAddrBook::CreateOneOff**erzeugt wird. 
  
Zum Erstellen eines Empfängers in einen bestimmten Container eingefügt werden soll, legen Sie _LpEidContainer_ auf Eintrags-ID und _CbEidContainer_ der Anzahl von Bytes in den Container Eintrags-ID des Containers. 
  
Um eine Vorlage verwenden, um einen Empfänger zu erstellen, legen Sie _LpEidNewEntryTpl_ auf die Eintrags-ID der zu verwendende Vorlage und _CbEidNewEntryTpl_ der Anzahl von Bytes in dieses Eintrags-ID ein. Die meisten änderbare Adresse Adressbuch Container unterstützen eine oder mehrere Vorlagen für die Erstellung eines bestimmten Typs Einträge. Einmalige-Vorlagen sind in der Regel, aber nicht immer, Dialogfelder. Eingeben von Informationen in die Vorlage erzeugt einen Empfänger mit einer Adresse, die für den Typ ordnungsgemäß formatiert ist. 
  
Erhalten Sie von einer Vorlage-Eintrags-ID:
  
- Die Spalte **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) des Containers einmaligen Tabelle, durch das Aufrufen des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode und zum Angeben von **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) als zugegriffen die Eigenschaftentag und IID_IMAPITable als Schnittstellenbezeichner. 
    
- Ein Adressbuch des Anbieters **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) Eigenschaften der Eintragsbezeichner halten Sie für die messaging-Benutzerobjekt des Anbieters und Verteilung von Listenvorlagen. 
    
> [!NOTE]
> Verwechseln Sie keinen neuen Eintrag Vorlage Eintrags-ID mit unterschiedliche Arten von Eintrags-ID eine ID für die Vorlage aufgerufen. Ein Vorlagenbezeichner ist nur von Anbietern zum Verwalten von anderen Anbietern kopierten Einträge verwendet; nie von Clients verwendet, und es wird nicht verwendet, um neue Einträge zu erstellen. 
  
Um den Typ des zu erstellenden Eintrags bestimmen der Benutzer zu aktivieren, übergeben Sie 0 (null) für _CbEidNewEntryTpl_ und NULL für _LpEidNewEntryTpl_. In diesem Fall **NewEntry** zeigt ein Standarddialogfeld aus einmaligen MAPIs-Tabelle erstellt – eine hierarchische Liste der alle Vorlagen, die von jedem Adressbuchanbieter im Profil unterstützt. 
  
Wenn ein Adresstyp festgelegt wurden, entweder durch die Einstellung des Parameters _LpEidNewEntryTpl_ oder eine Auswahl durch den Benutzer aus der einmaligen Tabellenanzeige, **NewEntry** entsprechende Vorlage seine zeigt die Tabelle zeigt. Alle neuen Eintrag Vorlagen unterstützen die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft. 
  
Damit **NewEntry** die Eintrags-ID des erstellten Eintrags zurückzugeben, übergeben Sie eine gültige Adresse für die Parameter _LpcbEidNewEntry_ und _LppEidNewEntry_ . MAPI platziert die neuen Eintrags-ID an die Adresse auf die _LppEidNewEntry_ und die Byteanzahl des neuen Eintrags-ID an der Adresse, die auf den _LpcbEidNewEntry_zeigt.
  
Rufen Sie [IABContainer::CreateEntry](iabcontainer-createentry.md) zum Erstellen eines Empfängers und speichern Sie es in einem bestimmten Adressbuchcontainer. Verwenden Sie diese Methode nur mit änderbare Containern – Container, denen die AB_MODIFIABLE flag festgelegt, in deren Eigenschaft **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Diese Methode unterstützt adressbuchanbietern implementierte mit veränderbaren Containern nicht. Geben Sie die Eintrags-ID der Vorlage für einen Eintrag mit dem gewünschten Typ in der _LpEntryID_ -Parameter erstellen. 
  
Geben Sie im _UlCreateFlags_ -Parameter die Art der Überprüfung der erforderlichen doppelter Eintrag und unabhängig davon, ob neue Einträge vorhandene ersetzen soll. Wenn **CreateEntry** zum Erstellen eines neuen Objekts aufgrund der doppelten Eintrag Überprüfung gemäß den Anbieter fehlschlägt, nicht erwarten Sie für einen Fehler oder eine Warnung zurückgegeben. Unter diesen Umständen Rückgabecode Anbieter einen Erfolg. 
  
Wenn Sie direkt mit einem Container arbeiten, und Sie wissen genau die Arten von Adressen, die der Container erstellen können, rufen Sie **IABContainer::CreateEntry** und übergeben Sie die Eintrags-ID für die geeignete Vorlage. Der Adressbuchanbieter legt einige Eigenschaften des ursprünglichen standardmäßigen fest. Rufen Sie **SetProps** , um andere Personen festzulegen. Der Benutzer ist nicht beteiligt. 
  

