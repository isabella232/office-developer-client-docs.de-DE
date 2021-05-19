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
  
Die [IABContainer::CopyEntries-Methode](iabcontainer-copyentries.md) Ihres Containers wird aufgerufen, wenn ein oder mehrere Empfänger aus demselben oder einem anderen Container in diesen Container kopiert werden sollen. **CopyEntries** verfügt über vier Eingabeparameter: ein Array von Eintragsbezeichnern, die die zu kopierenden Empfänger darstellen, ein Fensterhandle für die Statusanzeige, einen Statusobjektzeiger und einen Flagswert. Ihr Anbieter sollte den Fortschritt anzeigen, wenn AB_NO_DIALOG nicht festgelegt ist, und das Progress-Objekt aus dem  _lpProgress-Parameter_ verwenden, wenn es nicht NULL ist. Wenn  _lpProgress_ NULL ist, rufen [Sie IMAPISupport::D oProgressDialog auf,](imapisupport-doprogressdialog.md) um das MAPI-Progress-Objekt zu verwenden. Weitere Informationen zum Anzeigen des Fortschritts finden Sie unter [Displaying a Progress Indicator](mapi-progress-indicators.md).
  
Zusätzlich zu AB_NO_DIALOG, um einen Fortschrittsindikator zu unterdrücken, kann eines von zwei anderen Flags so festgelegt werden, dass eine Art doppelter Eintragsprüfungen CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT. Die CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT sind nur Vorschläge, wie Ihr Anbieter doppelte Einträge bestimmt und ignoriert werden kann. MAPI schlägt vor, dass Ihr Anbieter die Unterstützung für diese Flags wie folgt implementiert.
  
|**Doppeltes Eintragsflag**|**Vorgeschlagene Implementierung**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Überprüfen Sie, ob der Anzeigename im zu erstellende Eintrag dem Anzeigenamen eines Eintrags entspricht, der bereits im Container vorhanden ist.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Überprüfen Sie, ob sowohl der Anzeigename als auch der Suchschlüssel im zu erstellende Eintrag mit dem Anzeigenamen und dem Suchschlüssel eines Containereintrags übereinstimmen.  <br/> |
   
Das letzte Flag, CREATE_REPLACE, gibt an, dass der neue Eintrag den vorhandenen eintrag ersetzen soll, wenn Ihr Anbieter festgestellt hat, dass ein zu erstellende Eintrag ein Duplikat eines Eintrags ist, der bereits in Ihrem Container vorhanden ist. 
  
Wenn Ihr Anbieter ein persönliches Adressbuch ist, fügen Sie **die PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft in jeden Kopiervorgang ein. Wenn Sie die Detailanzeigetabelle eines kopierten Empfängers verwenden, kann ihr Container die Details des Empfängers anzeigen, anstatt den ursprünglichen Container aufrufen zu müssen, um die Anzeige zu erstellen.
  
 **So implementieren Sie IABContainer::CopyEntries**
  
1. Ermitteln Sie, ob sich jeder Eintragsbezeichner im  _lpEntries-Parameter_ in einem Format befindet, das von Ihrem Anbieter verarbeitet wird, und falls nicht, führen Sie fehler- und MAPI_E_INVALID_ENTRYID. 
    
2. Wenn ein Eintragsbezeichner einen Messagingbenutzer, eine Verteilerliste oder einen Container darstellt, den Ihr Anbieter verarbeitet:
    
1. Rufen Sie [Ihre IMAPISupport::OpenEntry-Methode](imapisupport-openentry.md) auf, um den entsprechenden Empfänger zu öffnen. 
    
2. Kopieren Sie den Empfänger in Ihren Container. 
    
3. Wenn der Eintragsbezeichner einen fremden Empfänger darstellt:
    
1. Rufen Sie die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) ihres Containers auf, um einen neuen Empfänger zu erstellen. 
    
2. Legen Sie die anfänglichen Eigenschaften für den neuen Empfänger ein.
    
4. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des neuen Objekts auf, um es zu speichern. 
    
5. Aktualisieren Sie die Inhaltstabelle des Containers so, dass sie den neuen Empfänger wiederspiegelt. 
    
6. Rufen [Sie IMAPISupport::Notify auf,](imapisupport-notify.md) um eine Tabellenbenachrichtigung an registrierte Clients zu senden. 
    

