---
title: Hinzufügen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421340"
---
# <a name="adding-address-book-entries"></a>Hinzufügen von Adressbucheinträgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um einem Container einen Messagingbenutzer oder eine Verteilerliste hinzuzufügen, Ruft ein Client [IAddrBook:: Neuentry](iaddrbook-newentry.md) auf, oder ein Anbieter ruft [IMAPISupport::](imapisupport-newentry.md) neueintrags mit dem Eintragsbezeichner des Zielcontainers im _lpEIDContainer_ -Parameter auf. MAPI ruft wiederum die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode des Containers auf, um den Eintrag mithilfe einer einmaligen Vorlage aus einer einmaligen Tabelle zu erstellen. Eine einmalige Vorlage ermöglicht es dem Client, einen neuen Empfänger eines bestimmten Typs zu erstellen. Die meisten Felder können bearbeitet werden. Die Vorlage, auf die durch den _lpEntryID_ -Parameter verwiesen wird, kann möglicherweise von Ihrem Anbieter bereitgestellt werden, oder es kann sich um eine Vorlage eines fremden Anbieters handeln, wenn Ihr Anbieter fremde Vorlagen unterstützt. Implementierungen **** von CreateEntry für Anbieter, die Empfänger aus einer fremden Vorlage erstellen können, sind immer komplexer als Implementierungen für Anbieter, die nicht. 
  
 **So implementieren Sie IABContainer:: createEntry**
  
1. Bestimmen des vom _lpEntryID_ -Parameter angegebenen Typs der Eintrags-ID. 
    
2. Wenn die Eintrags-ID eine Vorlage für einen Messagingbenutzer, eine Verteilerliste oder einen Adressbuchcontainer darstellt, die im Besitz Ihres Anbieters sind:
    
1. Erstellen und initialisieren Sie das entsprechende Objekt. Bei Bedarf kann Ihr Anbieter einige anfängliche Eigenschaften festlegen. Diese Eigenschaften hängen vom Typ des zu erstellenden Empfängers ab. 
    
2. Zurückgeben eines Zeigers auf die Implementierung des Objekts im Inhalt des _lppMAPIPropEntry_ -Parameters. 
    
3. Wenn die Eintrags-ID eine Vorlage für einen fremden Anbieter darstellt:
    
1. Rufen Sie [IMAPISupport:: OpenEntry](imapisupport-openentry.md) auf, um das fremdobjekt zu öffnen. 
    
2. Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Objekts auf, und übergeben Sie NULL für das Property-Tag-Array, um dessen Eigenschaften abzurufen. 
    
3. Bearbeiten Sie das von getProps **** zurückgegebene Eigenschafts Wertarray, indem Sie das Property-Tag in PR_NULL für alle Eigenschaften ändern, die für das neue Objekt nicht gelten und nicht übertragen werden sollen. 
    
4. Erstellen Sie eine Eintrags-ID für das neue Objekt. 
    
5. Erstellen Sie ein neues Objekt vom entsprechenden Typ, entweder Messaging-Benutzer oder Verteilerliste.
    
6. Initialisieren Sie das neue Objekt, indem Sie die Standardeigenschaften festlegen.
    
7. Überprüfen Sie, ob das Foreign-Objekt die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft unterstützt. 
    
8. Wenn das Foreign-Objekt **PR_TEMPLATEID**unterstützt, rufen Sie [IMAPISupport::](imapisupport-opentemplateid.md) opentemplatecode auf, um eine Property-Objekt Schnittstelle vom fremden Anbieter abzurufen, und legen Sie den Inhalt des _lppMAPIPropEntry_ -Parameters auf die Foreign-Eigenschaft fest. Objekt Implementierung. 
    
9. Wenn das Foreign-Objekt **PR_TEMPLATEID**nicht unterstützt, legen Sie die Inhalte des _lppMAPIPropEntry_ -Parameters auf die Implementierung des neuen Objekts durch den Anbieter fest. 
    
10. Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Objekts auf, auf das durch den _lppMAPIPropEntry_ -Parameter verwiesen wird, um die entsprechenden Eigenschaften aus dem Foreign-Objekt festzulegen. 
    

