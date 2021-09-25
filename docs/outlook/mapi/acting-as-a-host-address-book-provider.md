---
title: Fungieren als Hostadressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2e6bd9f2370b086ad3b53dd9db35116da374655e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567900"
---
# <a name="acting-as-a-host-address-book-provider"></a>Fungieren als Hostadressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Hostanbieter ist ein Adressbuchanbieter, der Empfänger von anderen Anbietern in seine Container einschließt und von der Implementierung der Empfänger durch die anderen Anbieter abhängt, um deren Wartung teilweise zu steuern. Ein Hostanbieter verwendet die Vorlagenbezeichner dieser fremden Empfänger, um die Daten für diese Empfänger an Code im fremden Anbieter zu binden. Dieser Bindungsprozess wird initiiert, wenn Ihr Anbieter die **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) -Eigenschaft eines Empfängers abruft und in einem Aufruf an [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)übergibt. 
  
Wenn Ihr Anbieter **IMAPISupport::OpenTemplateID aufruft,** gleicht MAPI die **MAPIUID** innerhalb des Vorlagenbezeichners mit einer **MAPIUID** ab, die von einem Anbieter registriert wurde, und ruft die [IABLogon::OpenTemplateID-Methode](iablogon-opentemplateid.md) des Anbieters auf. Der fremde Anbieter gibt möglicherweise einen Zeiger auf das Eigenschaftsobjekt des Anbieters, auf seine eigene Eigenschaftsobjektimplementierungen oder auf eine Implementierung zurück, die das Objekt des Anbieters umschließt. Der zurückgegebene Zeiger wird im Inhalt des  _lppMAPIPropNew-Parameters_ platziert. 
  
Ihr Anbieter kann auswählen, ob **IMAPISupport::OpenTemplateID** mit festgelegtem FILL_ENTRY-Flag aufgerufen werden soll. Legen Sie dieses Kennzeichen fest, wenn der Empfänger erstellt wird oder wenn eine lange Zeit vergangen ist, seit der Anbieter die Eigenschaften des Empfängers aktualisiert hat. Eine häufige Verwendung des FILL_ENTRY Flags besteht darin, einen Empfänger in Ihrem Anbieter mit dem Original synchronisiert zu halten. Die Implementierung dieser Art von Synchronisierungszeitplan verbessert die Leistung. 
  
 **So halten Sie einen Fremdempfänger synchronisiert**
  
1. Ermitteln Sie ein geeignetes Intervall für regelmäßige Updates. 
    
2. Zeitstempel für jeden Aufruf von [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Bewerten Sie, ob es erforderlich ist, eine vollständige Aktualisierung basierend auf der Zeitspanne durchzuführen, die seit dem letzten Aufruf abgelaufen ist. Wenn ein vollständiges Update erforderlich ist, rufen **Sie IMAPISupport::OpenTemplateID** mit dem Flag FILL_ENTRY auf. Wenn dies nicht erforderlich ist, legen Sie das Kennzeichen für den Anruf nicht fest. 
    
Wenn ein Client eine Anforderung für eine der Eigenschaften des kopierten Empfängers sendet, kann Ihr Anbieter auswählen, ob die Anforderung selbst verarbeitet oder der vom fremden Anbieter bereitgestellte Code verwendet werden soll. Ihr Anbieter kann davon ausgehen, dass der fremde Anbieter die meisten, wenn nicht alle Aufrufe von **IMAPIProp** abfangen wird, mit Ausnahme von [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Ein Aufruf von **OpenProperty,** der die **Eigenschaft PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) anfordert, wird immer an Ihren Anbieter weitergeleitet.
  
 **So greifen Sie auf den Vorlagenbezeichnercode zu**
  
1. Öffnen Sie den Empfänger, und rufen Sie seine [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) auf, um die **eigenschaft PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) abzurufen. Wenn **GetProps** fehlschlägt, weil **PR_TEMPLATEID** nicht verfügbar ist, unterstützt der fremde Anbieter keinen Vorlagenbezeichner und zugehörigen Code für diesen Empfänger. Ihr Anbieter muss die Implementierung des Empfängers für die gesamte Wartung verwenden. 
    
2. Wenn der Vorlagenbezeichner von **GetProps** zurückgegeben wird, übergeben Sie ihn und einen Zeiger an die **IMAPIProp-Implementierung** des Empfängers in einem Aufruf der **IMAPISupport::OpenTemplateID-Methode.** Legen Sie die FILL_ENTRY Kennzeichnung fest, wenn die meisten oder alle Eigenschaften des Empfängers aktualisiert werden müssen, z. B. zur Erstellungszeit oder wenn sie eine Weile nicht aktualisiert wurden. 
    
3. Wenn **OpenTemplateID** die **IMAPIProp-Implementierung** des fremdanbieters zurückgibt, kehren Sie zum Client einen Zeiger auf diese Implementierung zurück. 
    
4. Wenn **OpenTemplateID** keine Implementierung zurückgibt, in der Regel, weil sich der fremde Anbieter nicht im Profil befindet, kehren Sie zum Client einen Zeiger auf die **IMAPIProp-Implementierung** Ihres Anbieters zurück. Der Client sollte in der Lage sein, mit den Eigenschaften des Objekts über eine der beiden Schnittstellen zu arbeiten. 
    

