---
title: Fungieren als Host-Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 202d4b4391de7553e39e50dc527df5502ebcefb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406465"
---
# <a name="acting-as-a-host-address-book-provider"></a>Fungieren als Host-Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Hostanbieter ist ein Adressbuchanbieter, der Empfänger von anderen Anbietern in seinen Containern enthält und die Implementierung der Empfänger durch die anderen Anbieter verwendet, um die Wartung teilweise zu steuern. Ein Hostanbieter verwendet die Vorlagenbezeichner dieser fremden Empfänger, um die Daten für diese Empfänger an Code im fremden Anbieter zu binden. Dieser Bindungsprozess wird initiiert, wenn Ihr Anbieter die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft eines Empfängers abruft und diesen in einem Aufruf von [IMAPISupport::](imapisupport-opentemplateid.md)opentemplatecollection übergibt. 
  
Wenn Ihr Anbieter **IMAPISupport::** opentemplatecode aufruft, vergleicht MAPI die **MAPIUID** innerhalb des Vorlagen Bezeichners mit einem von einem Anbieter registrierten **MAPIUID** und ruft die [IABLogon:: OpenTemplate](iablogon-opentemplateid.md) -Methode des Anbieters auf. Der fremde Anbieter gibt möglicherweise einen Zeiger auf das Property-Objekt des Anbieters zurück, auf seine eigene Implementierung des Property-Objekts oder auf eine Implementierung, die das Objekt des Anbieters umschließt. Der zurückgegebene Zeiger wird in den Inhalt des _lppMAPIPropNew_ -Parameters gesetzt. 
  
Ihr Anbieter kann wählen, ob **IMAPISupport::** opentemplatecode mit dem FILL_ENTRY-Flagsatz aufgerufen werden soll. Legen Sie dieses Flag fest, wenn der Empfänger erstellt wird oder wenn eine lange Zeit vergangen ist, seit der Anbieter die Eigenschaften des Empfängers aktualisiert hat. Eine häufige Verwendung des FILL_ENTRY-Flags besteht darin, dass ein Empfänger in Ihrem Anbieter mit dem Original synchronisiert bleibt. Durch die Implementierung dieses Typs des Synchronisierungszeitplans wird die Leistung verbessert. 
  
 **So halten Sie einen fremden Empfänger synchronisiert**
  
1. Bestimmen Sie ein entsprechendes Intervall für regelmäßige Aktualisierungen. 
    
2. Zeitstempel für jeden Aufruf von [IMAPISupport::](imapisupport-opentemplateid.md)opentemplatecode. 
    
3. Bewerten Sie, ob es erforderlich ist, eine vollständige Aktualisierung basierend auf der Zeitdauer auszuführen, die seit dem letzten Aufruf abgelaufen ist. Wenn eine vollständige Aktualisierung erforderlich ist, rufen Sie **IMAPISupport::** opentemplatecode mit dem FILL_ENTRY-Flag auf. Wenn dies nicht erforderlich ist, legen Sie die Kennzeichnung für den Anruf nicht fest. 
    
Wenn ein Client eine Anforderung für eine der Eigenschaften des kopierten Empfängers stellt, kann der Anbieter auswählen, ob die Anforderung selbst verarbeitet werden soll, oder den vom fremden Anbieter bereitgestellten Code verwenden. Ihr Anbieter kann davon ausgehen, dass der ausländische Anbieter die meisten, wenn nicht alle, Aufrufe an **IMAPIProp** abfängt, mit Ausnahme von [IMAPIProp:: OpenProperty](imapiprop-openproperty.md). Ein Aufruf von **OpenProperty** , der die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft anfordert, wird immer an Ihren Anbieter weitergeleitet.
  
 **So greifen Sie auf den Code der Vorlagenkennung zu**
  
1. Öffnen Sie den Empfänger, und rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode auf, um die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft abzurufen. Wenn **** GetProps fehlschlägt, weil **PR_TEMPLATEID** nicht verfügbar ist, unterstützt der ausländische Anbieter keinen Vorlagenbezeichner und zugehörigen Code für diesen Empfänger. Ihr Anbieter muss seine Implementierung des Empfängers für alle Wartungsarbeiten verwenden. 
    
2. Wenn der Vorlagenbezeichner von getProps zurückgegeben wird, führen Sie ihn und einen Zeiger auf die **IMAPIProp** -Implementierung des Empfängers in einem Aufruf der **IMAPISupport::** opentemplatecollection-Methode. **** Legen Sie das FILL_ENTRY-Flag fest, wenn die meisten oder alle Eigenschaften des Empfängers aktualisiert werden müssen, beispielsweise zum Zeitpunkt der Erstellung oder wenn Sie für eine Weile nicht aktualisiert wurden. 
    
3. Wenn **** opentemplatecollection die **IMAPIProp** -Implementierung des fremden Anbieters zurückgibt, kehren Sie zum Client einen Zeiger auf diese Implementierung zurück. 
    
4. Wenn **** opentemplatecollection keine Implementierung zurückgibt, in der Regel, weil der fremde Anbieter nicht im Profil ist, kehren Sie zum Client einen Zeiger auf die **IMAPIProp** -Implementierung Ihres Anbieters zurück. Der Client sollte in der Lage sein, mit den Eigenschaften des Objekts über eine der beiden Schnittstellen zu arbeiten. 
    

