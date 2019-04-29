---
title: Kopieren von Adressbucheinträgen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418743"
---
# <a name="copying-address-book-entries"></a>Kopieren von Adressbucheinträgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [IABContainer:: CopyEntries](iabcontainer-copyentries.md) -Methode des Containers wird aufgerufen, wenn ein oder mehrere Empfänger aus demselben oder einem anderen Container in diesen Container kopiert werden sollen. **CopyEntries** verfügt über vier Eingabeparameter: ein Array von Eintrags-IDs, das die zu kopierenden Empfänger darstellt, ein Fensterhandle für die Statusanzeige, einen Statusobjekt Zeiger und einen Flags-Wert. Ihr Anbieter sollte den Fortschrittanzeigen, wenn das AB_NO_DIALOG-Flag nicht festgelegt ist, und das Progress-Objekt aus dem _lpProgress_ -Parameter verwenden, wenn es nicht NULL ist. Wenn _lpProgress_ ist, rufen Sie [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) auf, um das MAPI-Progress-Objekt zu verwenden. Weitere Informationen zum Anzeigen des Fortschritts finden Sie unter [Anzeigen einer Statusanzeige](mapi-progress-indicators.md).
  
Zusätzlich zu AB_NO_DIALOG, um eine Statusanzeige zu unterdrücken, kann eine der beiden anderen Flags so festgelegt werden, dass ein Typ doppelter Eintrags Überprüfung angefordert wird: CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT. Die Flags CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT sind nur Vorschläge, wie Ihr Anbieter doppelte Einträge bestimmt und ignoriert werden kann. MAPI schlägt vor, dass Ihr Anbieter die Unterstützung für diese Flags wie folgt implementiert.
  
|**Flag für doppelten Eintrag**|**Vorgeschlagene Implementierung**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Überprüfen Sie, ob der Anzeigename im zu erstellenden Eintrag mit dem Anzeigenamen eines Eintrags übereinstimmt, der sich bereits im Container befindet.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Überprüfen Sie, ob der Anzeigename und der Suchschlüssel im zu erstellenden Eintrag mit dem Anzeigenamen und dem Suchschlüssel eines Container Eintrags übereinstimmen.  <br/> |
   
Das letzte Flag, CREATE_REPLACE, gibt an, dass der neue Eintrag die vorhandene ersetzen soll, wenn Ihr Anbieter festgestellt hat, dass ein zu Erstell ender Eintrag ein Duplikat eines Eintrags in Ihrem Container ist. 
  
Wenn es sich bei Ihrem Anbieter um ein persönliches Adressbuch handelt, schließen Sie die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft in jeden Kopiervorgang ein. Das Einschließen der Details-Anzeigetabelle eines kopierten Empfängers ermöglicht es Ihrem Container, die Details des Empfängers anzuzeigen, statt den ursprünglichen Container aufrufen zu müssen, um die Anzeige zu erstellen.
  
 **So implementieren Sie IABContainer:: CopyEntries**
  
1. Bestimmen Sie, ob sich jede Eintrags-ID im _lpEntries_ -Parameter in einem Format befindet, das Ihr Anbieter verarbeitet, und wenn dies nicht der Fall ist, und geben Sie MAPI_E_INVALID_ENTRYID zurück. 
    
2. Wenn eine Eintrags-ID einen Messagingbenutzer, eine Verteilerliste oder einen Container darstellt, die der Anbieter behandelt:
    
1. Rufen Sie Ihre [IMAPISupport:: OpenEntry](imapisupport-openentry.md) -Methode auf, um den entsprechenden Empfänger zu öffnen. 
    
2. Kopieren Sie den Empfänger in ihren Container. 
    
3. Wenn die Eintrags-ID einen fremden Empfänger darstellt:
    
1. Rufen Sie die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode ihres Containers auf, um einen neuen Empfänger zu erstellen. 
    
2. Legen Sie die anfänglichen Eigenschaften für den neuen Empfänger fest.
    
4. Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des neuen Objekts auf, um Sie zu speichern. 
    
5. Aktualisieren Sie die Inhaltstabelle des Containers entsprechend dem neuen Empfänger. 
    
6. Rufen [Sie IMAPISupport:: notify](imapisupport-notify.md) auf, um eine Tabellenbenachrichtigung an registrierte Clients zu senden. 
    

