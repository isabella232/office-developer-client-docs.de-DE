---
title: Fungieren als fremder Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 300681bd585e9d534113404a82f43565f4e79bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435740"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Fungieren als fremder Adressbuchanbieter

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein fremder Anbieter ist ein Adressbuchanbieter, der: 
  
- Weist vorlagenbezeichner für die Empfänger zu.
    
- Unterstützt die [IABLogon::OpenTemplateID-Methode.](iablogon-opentemplateid.md) 
    
- Gibt Code zum Verwalten von Empfängern an, die in containern anderer Adressbuchanbieter vorhanden sind, die als Hostanbieter bezeichnet werden. Dieser Code umfasst ein Eigenschaftsobjekt, in der Regel eine IMAPIProp-Schnittstellenimplementierung, die ein Eigenschaftsobjekt vom Hostanbieter umschließt.  
    
Die Funktion als fremder Anbieter ist eine optionale Rolle. Nicht alle Anbieter müssen Vorlagenbezeichner und deren zugehörigen Code unterstützen. Implementieren Sie Ihren Anbieter als fremder Anbieter, wenn Sie die Kontrolle über Empfänger behalten möchten, die Hostanbieter mithilfe von Vorlagen ihres Anbieters erstellen. 
  
Das Format, das Ihr Anbieter für seine Eintragsbezeichner verwendet, kann auch für seine Vorlagenbezeichner verwendet werden. Vorlagenbezeichner müssen die registrierte **MAPIUID** Ihres Anbieters enthalten, damit MAPI Empfänger erfolgreich an die entsprechenden Anbieter binden kann. 
  
MAPI ruft die **IABLogon::OpenTemplateID-Methode** Ihres Anbieters auf, wenn ein Hostanbieter [IMAPISupport::OpenTemplateID aufruft.](imapisupport-opentemplateid.md) Der Hostanbieter übergibt den Vorlagenbezeichner des Empfängers im  _lpTemplateID-Parameter_ in seinem Aufruf an **IMAPISupport::OpenTemplateID**. MAPI bestimmt, dass die Vorlagen-ID zu Ihrem Anbieter gehört, indem sie die [MAPIUID](mapiuid.md) in der Vorlagen-ID mit der **MAPIUID** abgleicht, die Ihr Anbieter bei der Anmeldung registriert hat. MAPI gibt dann den Aufruf des Hostanbieters über die **IABLogon::OpenTemplateID-Methode** an Ihren Anbieter weiter. 
  
Der Hostanbieter übergibt außerdem einen Zeiger auf die Eigenschaftsobjektimplementierung für den Empfänger im  _lpMAPIPropData-Parameter,_ einen Schnittstellenbezeichner im  _lpInterface-Parameter,_ der dem Typ der in  _lpMAPIPropData_ übergebenen Schnittstellenimplementierung und einem optionalen Flag FILL_ENTRY. Ihr Anbieter soll im _lppMAPIPropNew-Parameter_ einen Zeiger auf eine Eigenschaftsobjektimplementierung des in _lpInterface angegebenen Typs zurückgeben._ Der zurückgegebene Zeiger kann entweder auf das von Ihrem Anbieter implementierte umschlossene Eigenschaftsobjekt oder auf das vom Hostanbieter in  _lpMAPIPropData_ bereitgestellte Objekt sein. Ihr Anbieter sollte einen umschlossenen Eigenschaftsobjektzeiger zurückgeben, wenn:
  
- Die Anzeigetabelle des Empfängers enthält Listenfeldsteuerelemente.
    
- Die E-Mail-Adresse für den Empfänger muss aus Daten in mehreren Anzeigetabelle-Steuerelementen zusammengesetzt werden.
    
- Ihr Anbieter gibt Probleme mit der Anzeige von Tabellenbenachrichtigungen auf.
    
Das FILL_ENTRY zeigt Ihrem Anbieter an, dass der Hostanbieter alle Eigenschaften des Empfängers aktualisieren muss. Ihr Anbieter muss diese Anforderung erfüllen.
  
Wenn ein Hostanbieter die **OpenTemplateID-Methode Ihres** Anbieters aufruft, kann ihr Anbieter: 
  
- Aktualisieren Sie regelmäßig die Daten für einen kopierten Eintrag.
    
- Halten Sie einen kopierten Eintrag mit dem Original synchronisiert, z. B. wenn ein Adressbucheintrag in das persönliche Adressbuch kopiert wird.
    
- Implementieren Sie Funktionen, die vom Hostanbieter nicht implementiert werden können, z. B. dynamisches Auffüllen von Listenfeldern in der Detailtabelle des kopierten Eintrags aus Daten auf einem Server.
    
- Steuern der Interaktion zwischen Eigenschaften in einem kopierten Eintrag oder einer instanziierten Vorlage. Beispielsweise wird das **PR_EMAIL_ADDRESS** von anderen In der Detailtabelle angezeigten Eigenschaften verwendet. 
    
Die ersten beiden Elemente sind Beispiele für Aufgaben, für die ihr Anbieter kein umschlossenes Eigenschaftsobjekt liefern muss – eine Implementierung von **IMAPIProp,** die auf der Implementierung des Hostanbieters basiert. Ihr Anbieter kann die Eigenschaften einfach bei Bedarf aktualisieren und zurückgeben und den  _lppMAPIPropNew-Parameter_ so festlegen, dass er auf den Zeiger verweist, der vom Hostanbieter im  _lpMAPIPropData-Parameter_ übergeben wird. 
  
Für die zweiten beiden Aufgaben muss Ihr Anbieter ein Eigenschaftsobjekt an den Hostanbieter zurückgeben, das das Objekt des Hostanbieters mit zusätzlichen Funktionen umschließt, z. B. die Möglichkeit, ein Eigenschaftenblatt für den Eintrag anzeigen zu können. Dieses Eigenschaftsobjekt ist entweder ein Messagingbenutzer oder eine Verteilerliste, abhängig vom Typ des Objekts, das vom Hostanbieter im  _lpMAPIPropData-Parameter_ übergeben und durch den Schnittstellenbezeichner im  _lpInterface-Parameter_ angegeben wird. Wenn der  _lpMAPIPropData-Parameter_ auf einen Messagingbenutzer verweist, muss das umschlossene Eigenschaftsobjekt ihres Anbieters eine **IMailUser-Implementierung** sein. Wenn _lpMAPIPropData_ auf eine Verteilerliste verweist, muss es sich um eine **IDistList-Implementierung.** 
  
Das umschlossene Eigenschaftsobjekt Ihres Anbieters fängt **IMAPIProp-Methodenaufrufe** ab, um kontextspezifische Manipulationen am Empfänger des Hostanbieters durchzuführen– dem Objekt, das umbrochen wird. MAPI hat nur eine Anforderung für umschlossene Eigenschaftsobjekte: Alle Aufrufe von [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) die die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft anfordern, sollten an den Hostanbieter übergeben werden. Die Implementierung Ihres Anbieters kann die zurückgegebene Tabelle verwenden, um Benachrichtigungen über Anzeigetabelle abzufangen oder bei Bedarf eigene hinzuzufügen. 
  
Die folgende Liste enthält Aufgaben, die in der Regel in dem umschlossenen Eigenschaftsobjekt implementiert werden, das von fremden Anbietern implementiert wird:
  
- Werte der Vorverarbeitungs- und Postverarbeitungseigenschaft für den Hostempfänger in [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Behandeln von Details anzeigen Tabellensteuerelemente, z. B. Schaltflächen und Listenfelder, in **IMAPIProp::OpenProperty**.
    
- Überprüfen oder Bearbeiten von Eigenschaftswerten für den Hostempfänger in [IMAPIProp::SetProps](imapiprop-setprops.md).
    
- Berechnen erforderlicher Eigenschaften wie **PR_EMAIL_ADDRESS** und Überprüfen, ob alle erforderlichen Eigenschaften festgelegt wurden, bevor der Hostempfänger in [IMAPIProp::SaveChanges](imapiprop-savechanges.md)gespeichert wird.
    
### <a name="to-implement-iablogonopentemplateid"></a>So implementieren Sie IABLogon::OpenTemplateID
  
1. Überprüfen Sie, ob der vorlagenbezeichner, der mit dem  _lpTemplateID-Parameter_ übergeben wurde, gültig ist und ein Format hat, das ihr Anbieter erkennt. Andern falls nicht, führen Sie einen Fehler aus, und geben Sie MAPI_E_INVALID_ENTRYID. 
    
2. Erstellen Sie ein Objekt des Typs, der durch den Vorlagenbezeichner angegeben ist, entweder ein Messagingbenutzer, eine Verteilerliste oder ein einmal verwendeter Empfänger. 
    
3. Rufen Sie **die IUnknown::AddRef-Methode** im Eigenschaftsobjekt des Hostanbieters auf, auf das das Objekt verweist, auf das der  _lpMAPIPropData-Parameter_ verweist. 
    
4. Wenn der  _ulTemplateFlags-Parameter_ auf "FILL_ENTRY: 
    
   1. Wenn es sich bei dem neuen Objekt um einen Messagingbenutzer oder eine Verteilerliste handelt:
      
      1. Rufen Sie alle Eigenschaften des neuen Objekts ab, möglicherweise durch Aufrufen der **IMAPIProp::GetProps-Methode.** 
          
      2. Rufen Sie die **IMAPIProp::SetProps-Methode** des Hostanbieters auf, um alle abgerufenen Eigenschaften in das Eigenschaftsobjekt des Hostanbieters zu kopieren. 
      
   2. Wenn es sich bei dem neuen Objekt um einen einmal verwendeten Empfänger handelt, rufen Sie die **IMAPIProp::SetProps-Methode** des Hostanbieters auf, um die folgenden Eigenschaften zu setzen: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) an den Adresstyp an, der von Ihrem Anbieter verarbeitet wird.
        
      - **PR \_ TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) zum Vorlagenbezeichner aus den _Parametern lpTemplateID_ und _cbTemplateID._ 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) zu DT_MAILUSER oder DT_DISTLIST, wenn dies der Richtige ist.
    
5. Legen Sie den Inhalt des  _lppMAPIPropNew-Parameters_ so fest, dass er entweder auf das neue Objekt Ihres Anbieters oder auf das eigenschaftsobjekt verweisen soll, das mit dem  _lpMAPIPropData-Parameter_ übergeben wird, je nachdem, ob ihr Anbieter bestimmt, dass ein umschlossenes Objekt erforderlich ist. 
    
6. Wenn ein kritischer Fehler auftritt, z. B. ein Netzwerkfehler oder eine Nichtspeicherbedingung, geben Sie den entsprechenden Fehlerwert zurück. Dieser Wert sollte an den Client mit der entsprechenden [MAPIERROR-Struktur,](mapierror.md) einer Aufgabe, die vom Hostanbieter ausgeführt wird, verbreitet werden. 
    

