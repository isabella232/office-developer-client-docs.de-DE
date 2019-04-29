---
title: Anzeigen von Empfängerinformationen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412954"
---
# <a name="displaying-recipient-information"></a>Anzeigen von Empfängerinformationen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet ein allgemeines Dialogfeld zum Anzeigen von Empfängerdetails. Das Dialogfeld Details wird aus einer Anzeigetabelle und einer **IMAPIProp** -Implementierung erstellt. In der Anzeigetabelle wird die Darstellung der Details angezeigt, und die **IMAPIProp** -Implementierung steuert die Daten für den Empfänger. Ihr Anbieter ist für die Bereitstellung der Anzeigetabelle und der **IMAPIProp** -Implementierung für jeden Empfänger verantwortlich. 
  
Am einfachsten können Sie die Anzeigetabelle erstellen, indem Sie eine [DTPAGE](dtpage.md) -Struktur definieren und [BuildDisplayTable](builddisplaytable.md)aufrufen. Einige Anbieter, insbesondere schreibgeschützte Anbieter, die das Erstellen von einmaligen Empfängern zulassen, verwenden jedoch **IPropData**. Bei der **IMAPIProp** -Implementierung kann es sich um einen beliebigen Typ von Property-Objekt handeln. 
  
Es gibt zwei Methoden zum Aufrufen dieses Dialogfelds: [IAddrBook::D ails](iaddrbook-details.md) und [IMAPISupport::D ails](imapisupport-details.md). Wenn der Anbieter eine dieser Methoden zum Anfordern von Details für einen Empfänger aufruft, wird der Empfänger von MAPI zunächst durch Aufrufen der [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) -Methode des Containers geöffnet. Als nächstes wird die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Empfängers aufgerufen, um die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft anzufordern. **PR_DETAILS_TABLE** ist die Eigenschaft, die die Details der Anzeigetabelle eines Empfängers darstellt. 
  
Die [IPropData: IMAPIProp](ipropdataimapiprop.md) -Schnittstelle kann verwendet werden, um Änderungen an Anzeige Tabellensteuerelemente zu überwachen, wie im folgenden Verfahren beschrieben. 
  
## <a name="monitor-changes-to-a-control"></a>Überwachen von Änderungen an einem Steuerelement
  
1. Bevor der Benutzer Zugriff auf das Steuerelement erhält, rufen Sie [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) auf, um den Zugriff auf IPROP_CLEAN für den Steuerelement festzulegen. 
    
2. Ermöglicht dem Benutzer das Arbeiten mit dem Dialogfeld. 
    
3. Wenn der Benutzer fertig ist, rufen Sie [IPropData:: HrGetPropAccess](ipropdata-hrgetpropaccess.md) auf, um die aktuelle Zugriffsebene des Steuerelements abzurufen. 
    
4. Wenn die Zugriffsebene IPROP_DIRTY ist, hat der Benutzer das Steuerelement geändert. Ihr Anbieter sollte:
    
   - Rufen Sie [IPropData:: HrSetPropAccess](ipropdata-hrsetpropaccess.md) auf, um die Zugriffsebene auf IPROP_CLEAN zurückzustellen. 
    
   - Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Property-Datenobjekts auf, um die geänderte Eigenschaft abzurufen und durch Aufrufen von [IMAPIProp::](imapiprop-setprops.md)SetProps zu aktualisieren.
    
5. Wenn die Zugriffsebene immer noch IPROP_CLEAN ist, wurde das Steuerelement nicht geändert. 
    
Weitere Informationen zum Erstellen von Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).
  

