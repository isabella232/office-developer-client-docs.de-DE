---
title: Kopieren von Adressbucheinträgen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ced6f77a73c8b0bb93cf464226ba254d357c098b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617020"
---
# <a name="copying-address-book-entries"></a>Kopieren von Adressbucheinträgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [IABContainer::CopyEntries-Methode](iabcontainer-copyentries.md) Ihres Containers wird aufgerufen, wenn mindestens ein Empfänger aus demselben oder einem anderen Container in diesen Container kopiert werden soll. **CopyEntries** verfügt über vier Eingabeparameter: ein Array von Eintragsbezeichnern, die die zu kopierenden Empfänger darstellen, ein Fensterhandle für die Statusanzeige, einen Statusobjektzeiger und einen Flags-Wert. Der Anbieter sollte den Fortschritt anzeigen, wenn das AB_NO_DIALOG-Flag nicht festgelegt ist, und das Statusobjekt aus dem  _lpProgress-Parameter_ verwenden, wenn es nicht NULL ist. Wenn  _lpProgress_ NULL ist, rufen Sie [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) auf, um das MAPI-Statusobjekt zu verwenden. Weitere Informationen zum Anzeigen des Fortschritts finden Sie unter [Anzeigen einer Statusanzeige.](mapi-progress-indicators.md)
  
Zusätzlich zu AB_NO_DIALOG, um eine Statusanzeige zu unterdrücken, kann eines von zwei anderen Flags so festgelegt werden, dass eine Art doppelter Eintragsprüfung angefordert wird: CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT. Die Flags CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT sind nur Vorschläge, wie Ihr Anbieter doppelte Einträge ermittelt und ignoriert werden kann. Mapi schlägt vor, dass Ihr Anbieter unterstützung für diese Flags wie folgt implementiert.
  
|**Doppelte Eintragskennzeichnung**|**Vorgeschlagene Implementierung**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Überprüfen Sie, ob der Anzeigename im zu erstellenden Eintrag mit dem Anzeigenamen eines Eintrags übereinstimmt, der sich bereits im Container befindet.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Überprüfen Sie, ob sowohl der Anzeigename als auch der Suchschlüssel im zu erstellenden Eintrag mit dem Anzeigenamen und dem Suchschlüssel eines Containereintrags übereinstimmen.  <br/> |
   
Das letzte Flag, CREATE_REPLACE, gibt an, dass der neue Eintrag den vorhandenen ersetzen soll, wenn der Anbieter festgestellt hat, dass ein zu erstellende Eintrag ein Duplikat eines Eintrags ist, der sich bereits in Ihrem Container befindet. 
  
Wenn Ihr Anbieter ein persönliches Adressbuch ist, schließen Sie die **Eigenschaft PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) in jeden Kopiervorgang ein. Wenn Sie die Detailanzeigetabelle eines kopierten Empfängers einschließen, kann Ihr Container die Details des Empfängers anzeigen, anstatt den ursprünglichen Container aufrufen zu müssen, um die Anzeige zu erstellen.
  
 **So implementieren Sie IABContainer::CopyEntries**
  
1. Ermitteln Sie, ob jeder Eintragsbezeichner im  _LpEntries-Parameter_ ein Format aufweist, das vom Anbieter behandelt wird, und wenn dies nicht der Typ ist, schlagen Sie fehl, und geben Sie MAPI_E_INVALID_ENTRYID zurück. 
    
2. Wenn ein Eintragsbezeichner einen Messagingbenutzer, eine Verteilerliste oder einen Container darstellt, den Ihr Anbieter verarbeitet:
    
1. Rufen Sie Ihre [IMAPISupport::OpenEntry-Methode](imapisupport-openentry.md) auf, um den entsprechenden Empfänger zu öffnen. 
    
2. Kopieren Sie den Empfänger in Ihren Container. 
    
3. Wenn der Eintragsbezeichner einen fremden Empfänger darstellt:
    
1. Rufen Sie die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) Ihres Containers auf, um einen neuen Empfänger zu erstellen. 
    
2. Legen Sie die anfänglichen Eigenschaften für den neuen Empfänger fest.
    
4. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des neuen Objekts auf, um es zu speichern. 
    
5. Aktualisieren Sie das Inhaltsverzeichnis des Containers, um den neuen Empfänger widerzuspiegeln. 
    
6. Rufen Sie [IMAPISupport::Notify](imapisupport-notify.md) auf, um eine Tabellenbenachrichtigung an registrierte Clients zu senden. 
    

