---
title: Fungieren als fremder Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c72269d09e4b14f86e08a848084645aca7f6ca61
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567921"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Fungieren als fremder Adressbuchanbieter

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein fremder Anbieter ist ein Adressbuchanbieter, der: 
  
- Weist den Empfängern Vorlagenbezeichner zu.
    
- Unterstützt die [IABLogon::OpenTemplateID-Methode.](iablogon-opentemplateid.md) 
    
- Stellt Code zum Verwalten von Empfängern bereit, die in containern anderer Adressbuchanbieter vorhanden sind, die als Hostanbieter bezeichnet werden. Dieser Code umfasst ein Eigenschaftsobjekt, in der Regel eine IMAPIProp-Schnittstellenimplementierungen, die ein Eigenschaftsobjekt vom Hostanbieter umschließen.  
    
Die Funktion als fremder Anbieter ist eine optionale Rolle. Nicht alle Anbieter müssen Vorlagenbezeichner und deren zugehörigen Code unterstützen. Implementieren Sie Ihren Anbieter als fremder Anbieter, wenn Sie die Kontrolle über Empfänger behalten möchten, die Hostanbieter mithilfe der von Ihrem Anbieter bereitgestellten Vorlagen erstellen. 
  
Das Format, das Ihr Anbieter für seine Eintragsbezeichner verwendet, kann auch für seine Vorlagenbezeichner verwendet werden. Vorlagenbezeichner müssen die registrierte **MAPIUID** Ihres Anbieters enthalten, damit MAPI Empfänger erfolgreich an die entsprechenden Anbieter binden kann. 
  
MAPI ruft die **IABLogon::OpenTemplateID-Methode** Ihres Anbieters auf, wenn ein Hostanbieter [IMAPISupport::OpenTemplateID aufruft.](imapisupport-opentemplateid.md) Der Hostanbieter übergibt den Vorlagenbezeichner des Empfängers im Parameter  _lpTemplateID_ in seinem Aufruf an **IMAPISupport::OpenTemplateID**. MAPI ermittelt, dass der Vorlagenbezeichner zu Ihrem Anbieter gehört, indem die [MAPIUID](mapiuid.md) im Vorlagenbezeichner mit der **MAPIUID** übereinstimmt, die Ihr Anbieter bei der Anmeldung registriert hat. MapI leitet dann den Aufruf des Hostanbieters über die **IABLogon::OpenTemplateID-Methode** an Ihren Anbieter weiter. 
  
Der Hostanbieter übergibt auch einen Zeiger auf seine Eigenschaftsobjektimplementierung für den Empfänger im Parameter  _lpMAPIPropData,_ einen Schnittstellenbezeichner im  _lpInterface-Parameter,_ der dem Typ der in  _lpMAPIPropData_ übergebenen Schnittstellenimplementierung entspricht, und ein optionales Flag, FILL_ENTRY. Es wird erwartet, dass ihr Anbieter im  _lppMAPIPropNew-Parameter_ einen Zeiger auf eine Eigenschaftsobjektimplementierungen des in  _lpInterface_ angegebenen Typs zurückgibt. Der zurückgegebene Zeiger kann entweder auf das vom Anbieter implementierte wrapped-Eigenschaftsobjekt oder auf das vom Hostanbieter in  _lpMAPIPropData_ bereitgestellte Objekt verweisen. Ihr Anbieter sollte einen umschlossenen Eigenschaftenobjektzeiger zurückgeben, wenn:
  
- Die Anzeigetabelle des Empfängers enthält Listenfeld-Steuerelemente.
    
- Die E-Mail-Adresse für den Empfänger muss aus Daten in mehreren Anzeigetabellensteuerelementen zusammengestellt werden.
    
- Ihre Anbieterprobleme zeigen Tabellenbenachrichtigungen an.
    
Das flag FILL_ENTRY gibt Ihrem Anbieter an, dass für den Hostanbieter alle Eigenschaften des Empfängers aktualisiert werden müssen. Ihr Anbieter ist erforderlich, um diese Anforderung zu erfüllen.
  
Wenn ein Hostanbieter die **OpenTemplateID-Methode** Ihres Anbieters aufruft, kann ihr Anbieter Folgendes tun: 
  
- Aktualisieren Sie in regelmäßigen Abständen die Daten für einen kopierten Eintrag.
    
- Lassen Sie einen kopierten Eintrag mit seinem Original synchronisiert, z. B. wenn ein Adressbucheintrag in das persönliche Adressbuch kopiert wird.
    
- Implementieren Sie Funktionen, die vom Hostanbieter nicht implementiert werden können, z. B. dynamisches Auffüllen von Listenfeldern in der Detailtabelle des kopierten Eintrags aus Daten auf einem Server.
    
- Steuern der Interaktion zwischen Eigenschaften in einem kopierten Eintrag oder einer instanziierten Vorlage. Beispiel: Berechnen **von PR_EMAIL_ADDRESS** aus anderen Eigenschaften, die in der Detailtabelle angezeigt werden. 
    
Die ersten beiden Elemente sind Beispiele für Aufgaben, bei denen ihr Anbieter kein umschlossenes Eigenschaftsobjekt bereitstellen muss – eine Implementierung von **IMAPIProp,** die auf der Implementierung des Hostanbieters basiert. Ihr Anbieter kann die Eigenschaften einfach nach Bedarf aktualisieren und zurückgeben, indem er den  _Parameter "lppMAPIPropNew"_ so festlegt, dass er auf den zeiger verweist, der vom Hostanbieter im  _Parameter "lpMAPIPropData"_ übergeben wird. 
  
Die zweiten beiden Aufgaben erfordern, dass Ihr Anbieter zum Hostanbieter ein Eigenschaftsobjekt zurückgibt, das das Objekt des Hostanbieters mit zusätzlichen Funktionen umschließt, z. B. der Möglichkeit, ein Eigenschaftenblatt für den Eintrag anzuzeigen. Dieses Eigenschaftsobjekt ist entweder ein Messagingbenutzer oder eine Verteilerliste, abhängig vom Typ des Objekts, das vom Hostanbieter im  _parameter lpMAPIPropData_ übergeben und durch den Schnittstellenbezeichner im  _lpInterface-Parameter_ angegeben wird. Wenn der  _parameter lpMAPIPropData_ auf einen Messagingbenutzer zeigt, muss das umschlossene Eigenschaftsobjekt des Anbieters eine **IMailUser-Implementierung** sein. Wenn _lpMAPIPropData_ auf eine Verteilerliste verweist, muss es sich um eine **IDistList-Implementierung handelt.** 
  
Das umschlossene Eigenschaftsobjekt Ihres Anbieters fängt **IMAPIProp-Methodenaufrufe** ab, um eine kontextspezifische Manipulation des Empfängers des Hostanbieters durchzuführen – das Objekt, das umgebrochen wird. MAPI hat nur eine Anforderung für umschlossene Eigenschaftsobjekte: Alle Aufrufe von [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) die die **eigenschaft PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) anfordern, sollten an den Hostanbieter übergeben werden. Die Implementierung Ihres Anbieters kann die zurückgegebene Tabelle verwenden, um Tabellenbenachrichtigungen abzufangen oder bei Bedarf eine eigene hinzuzufügen. 
  
Die folgende Liste enthält Aufgaben, die in der Regel in dem umschlossenen Eigenschaftsobjekt implementiert werden, das von fremden Anbietern implementiert wird:
  
- Werte der Vor- und Nachbearbeitungseigenschaft für den Hostempfänger in [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Behandeln von Details zeigen Tabellensteuerelemente wie Schaltflächen und Listenfelder in **IMAPIProp::OpenProperty** an.
    
- Überprüfen oder Bearbeiten von Eigenschaftswerten für den Hostempfänger in [IMAPIProp::SetProps](imapiprop-setprops.md).
    
- Berechnen erforderlicher Eigenschaften wie **PR_EMAIL_ADDRESS** und Überprüfen, ob alle erforderlichen Eigenschaften festgelegt wurden, bevor der Hostempfänger in [IMAPIProp::SaveChanges](imapiprop-savechanges.md)gespeichert wird.
    
### <a name="to-implement-iablogonopentemplateid"></a>So implementieren Sie IABLogon::OpenTemplateID
  
1. Überprüfen Sie, ob der mit dem  _parameter lpTemplateID übergebene_ Vorlagenbezeichner gültig ist und ein Format aufweist, das ihr Anbieter erkennt. Ist dies nicht der Typ, schlagen Sie fehl, und geben Sie MAPI_E_INVALID_ENTRYID zurück. 
    
2. Erstellen Sie ein Objekt vom Typ, der durch den Vorlagenbezeichner angegeben wird, entweder ein Messagingbenutzer, eine Verteilerliste oder ein einmaliger Empfänger. 
    
3. Rufen Sie die **IUnknown::AddRef-Methode** im Eigenschaftsobjekt des Hostanbieters auf, auf das durch den  _Parameter lpMAPIPropData_ verwiesen wird. 
    
4. Wenn der  _ulTemplateFlags-Parameter_ auf FILL_ENTRY festgelegt ist: 
    
   1. Wenn es sich bei dem neuen Objekt um einen Messagingbenutzer oder eine Verteilerliste handelt:
      
      1. Rufen Sie alle Eigenschaften des neuen Objekts ab, möglicherweise durch Aufrufen der **IMAPIProp::GetProps-Methode.** 
          
      2. Rufen Sie die **IMAPIProp::SetProps-Methode** des Hostanbieters auf, um alle abgerufenen Eigenschaften in das Eigenschaftenobjekt des Hostanbieters zu kopieren. 
      
   2. Wenn das neue Objekt ein einmaliger Empfänger ist, rufen Sie die **IMAPIProp::SetProps-Methode** des Hostanbieters auf, um die folgenden Eigenschaften festzulegen: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) zum Adresstyp, der von Ihrem Anbieter verarbeitet wird.
        
      - **PR \_ TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) zum Vorlagenbezeichner aus den _Parametern lpTemplateID_ und _cbTemplateID._ 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) nach Bedarf DT_MAILUSER oder DT_DISTLIST.
    
5. Legen Sie den Inhalt des  _lppMAPIPropNew-Parameters_ so fest, dass er auf das neue Objekt des Anbieters oder auf das eigenschaftenobjekt verweist, das mit dem  _Parameter lpMAPIPropData_ übergeben wird, je nachdem, ob der Anbieter ein umschlossenes Objekt bestimmt, das erforderlich ist. 
    
6. Wenn ein schwerwiegender Fehler auftritt, z. B. ein Netzwerkfehler oder eine Nicht-Arbeitsspeicher-Bedingung, geben Sie den entsprechenden Fehlerwert zurück. Dieser Wert sollte mit der entsprechenden [MAPIERROR-Struktur,](mapierror.md) einer vom Hostanbieter ausgeführten Aufgabe, an den Client weitergegeben werden. 
    

