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
ms.openlocfilehash: eca0c9f63a4efaaa7f9fd066cf5dce451b8f6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565886"
---
# <a name="copying-address-book-entries"></a>Kopieren von Adressbucheinträgen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
[IABContainer::CopyEntries](iabcontainer-copyentries.md) -Methode des Containers wird aufgerufen, wenn eine oder mehrere Empfänger aus der gleichen oder einen anderen Container sind in diesen Container kopiert werden. **CopyEntries** hat vier Eingabeparameter: ein Array von Eintragsbezeichner, die die Empfänger zu kopierenden darstellt, die ein Fensterhandle für die Statusanzeige, einem Objektverweis Fortschritt und ein Flagwert. Der Anbieter sollte Fortschritt angezeigt werden, wenn das Flag AB_NO_DIALOG nicht festgelegt ist und das Fortschritt-Objekt aus der _LpProgress_ -Parameter verwenden, wenn es nicht NULL ist. Wenn _LpProgress_ NULL ist, rufen Sie [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) zum Verwenden des MAPI-Objekts ausgeführt. Weitere Informationen zum Anzeigen des Fortschritts finden Sie unter [eine Statusanzeige anzeigen](mapi-progress-indicators.md).
  
Zusätzlich zu AB_NO_DIALOG unterdrückt werden, eine Statusanzeige, kann eines der beiden anderen Kennzeichen auf ein doppelter Eintrag überprüfen angefordert festgelegt werden: CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT. Die Flags CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT sind nur Vorschläge, wie vom Dienstanbieter doppelte Einträge bestimmt und können ignoriert werden. MAPI impliziert, dass der Anbieter Unterstützung für diese Flags wie folgt implementieren.
  
|**Doppelter Eintrag Kennzeichnung**|**Vorgeschlagene Implementierung**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Überprüfen Sie, ob der Anzeigename in den Eintrag zu erstellenden den Anzeigenamen eines Eintrags bereits im Container entspricht.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Überprüfen Sie, ob den Anzeigenamen und die suchen-Taste in den Eintrag erstellt werden mit dem Display Name, und suchen Sie Key eines Eintrags Container übereinstimmen.  <br/> |
   
Das letzte-Flag CREATE_REPLACE, gibt an, dass der neue Eintrag vorhandenen ersetzen soll, falls es sich bei Ihrem Anbieter festgestellt hat, dass ein Eintrag erstellt werden soll ein Duplikat des Eintrags bereits in Ihrer Container ist. 
  
Wenn Ihr Anbieter ein persönliches Adressbuch ist, fügen Sie die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft in jedem Kopiervorgang. Zeigt die Tabelle die Details eines Empfängers kopierten einschließlich ermöglicht den Container zum Anzeigen der Details der Empfänger und erspart den ursprünglichen Container aufrufen, um die Anzeige zu erstellen.
  
 **Implementieren von IABContainer::CopyEntries**
  
1. Ermitteln Sie, ob jede Eintrags-ID in der _LpEntries_ -Parameter in einem Format, die vom Dienstanbieter behandelt und wird ist dies nicht, ein Fehler auftritt und MAPI_E_INVALID_ENTRYID zurückzugeben. 
    
2. Wenn eine Eintrags-ID darstellt, eine messaging-Benutzer, Verteilerliste oder Container für die Behandlung von Ihrem Anbieter:
    
1. Rufen Sie eine [IMAPISupport::OpenEntry](imapisupport-openentry.md) -Methode, um den entsprechenden Empfänger zu öffnen. 
    
2. Kopieren Sie den Empfänger in den Container. 
    
3. Wenn die Eintrags-ID einen fremden Empfänger darstellt:
    
1. Aufrufen des Containers [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um einen neuen Empfänger zu erstellen. 
    
2. Festlegen von ursprünglichen Eigenschaften für den neuen Empfänger.
    
4. Rufen Sie das neue Objekt [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um es zu speichern. 
    
5. Aktualisieren Sie den Container Inhaltstabelle entsprechend den neuen Empfänger. 
    
6. Rufen Sie [IMAPISupport::Notify](imapisupport-notify.md) , um eine Tabelle Benachrichtigung an registrierte Clients zu senden. 
    

