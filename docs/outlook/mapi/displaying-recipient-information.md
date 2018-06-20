---
title: Anzeigen von Empfängerinformationen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7071c05f6f59740163f97f840c7fa48d83bea815
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791575"
---
# <a name="displaying-recipient-information"></a>Anzeigen von Empfängerinformationen

**Betrifft**: Outlook 
  
MAPI bietet ein Standarddialogfeld für Empfänger-Details anzeigen. Im Dialogfeld Details der wird aus einer Tabelle anzeigen und eine Implementierung **IMAPIProp** erstellt. Zeigt die Tabelle erläutert, wie unter "Details" und die Implementierung **IMAPIProp** steuert die Daten für den Empfänger. Der Anbieter ist verantwortlich für die Angabe der Tabelle anzeigen und die Implementierung **IMAPIProp** für jeden Empfänger. 
  
Die einfachste Möglichkeit zum Erstellen der Anzeige-Tabelle ist eine Struktur [DTPAGE](dtpage.md) definieren und Aufrufen von [BuildDisplayTable](builddisplaytable.md). Verwenden Sie einige Anbieter, insbesondere schreibgeschützte Anbieter, mit denen die Erstellung von einmaligen Empfängern können jedoch **IPropData**. Die Implementierung **IMAPIProp** kann jede Art von Property-Objekt sein. 
  
Es gibt zwei Methoden zum Aufrufen dieses Dialogfeld: [IAddrBook::Details](iaddrbook-details.md) und [IMAPISupport::Details](imapisupport-details.md). Wenn der Anbieter eine der folgenden Methoden zum Anfordern von Informationen für einen Empfänger aufruft, öffnet MAPI zuerst den Empfänger durch Aufrufen des Containers [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) -Methode. Danach wird der Aufgabenliste des Empfängers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, um anzufordern, die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft. **PR_DETAILS_TABLE** ist die Eigenschaft, die einen Empfänger Details zeigt die Tabelle darstellt. 
  
Die [IPropData: IMAPIProp](ipropdataimapiprop.md) -Schnittstelle verwendet werden, um Änderungen auf die Tabellensteuerelemente anzeigen zu überwachen, wie im folgenden Verfahren beschrieben. 
  
## <a name="monitor-changes-to-a-control"></a>Überwachen von Änderungen an ein Steuerelement
  
1. Bevor der Benutzer Zugriff auf das Steuerelement erhält, rufen Sie [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) , um die Steuerung des Zugriffs auf IPROP_CLEAN festzulegen auf. 
    
2. Ermöglicht es dem Benutzer das Dialogfeld entwickelt. 
    
3. Wenn der Benutzer beendet wurde, rufen Sie [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) zum Abrufen der aktuellen Zugriffsebene des Steuerelements. 
    
4. Wenn die Zugriffsebene IPROP_DIRTY ist, hat der Benutzer das Steuerelement geändert. Der Anbieter sollte:
    
   - Rufen Sie wieder auf IPROP_CLEAN [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , um den Zugriff festzulegen. 
    
   - Rufen Sie die Eigenschaft Datenobjekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, um die geänderte Eigenschaft abgerufen und durch Aufrufen von [IMAPIProp::SetProps](imapiprop-setprops.md)zu aktualisieren.
    
5. Wenn die Zugriffsebene noch IPROP_CLEAN ist, wurde das Steuerelement nicht geändert. 
    
Weitere Informationen zum Erstellen von Tabellen anzeigen finden Sie unter [Tabellen angezeigt](display-tables.md).
  

