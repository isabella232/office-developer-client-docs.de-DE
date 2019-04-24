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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331209"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Fungieren als fremder Adressbuchanbieter

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein ausländischer Anbieter ist ein Adressbuchanbieter, der: 
  
- Weist den Empfängern Vorlagenbezeichner zu.
    
- Unterstützt die [IABLogon::](iablogon-opentemplateid.md) opentemplatecollection-Methode. 
    
- Stellt Code zum Verwalten von Empfängern bereit, die in den Containern anderer Adressbuchanbieter vorhanden sind, die als Hostanbieter bezeichnet werden. Dieser Code umfasst ein Property-Objekt, in der Regel eine **IMAPIProp** -Schnittstellenimplementierung, die ein Property-Objekt vom Hostanbieter umschließt. 
    
Als ausländischer Anbieter handelt es sich um eine optionale Rolle. nicht alle Anbieter müssen Vorlagenbezeichner und den dazugehörigen Code unterstützen. Implementieren Sie Ihren Anbieter als fremden Anbieter, wenn Sie die Kontrolle über Empfänger behalten möchten, die von Hostanbietern mithilfe von Vorlagen bereitgestellt werden. 
  
Das Format, das Ihr Anbieter für seine Eintrags-IDs verwendet, kann auch für seine Vorlagenbezeichner verwendet werden. Vorlagenbezeichner müssen die registrierten **MAPIUID** Ihres Anbieters aufweisen, damit MAPI die Empfänger erfolgreich an die entsprechenden Anbieter binden kann. 
  
MAPI Ruft die **IABLogon::** opentemplatecode-Methode Ihres Anbieters auf, wenn ein Hostanbieter [IMAPISupport::](imapisupport-opentemplateid.md)opentemplatecollection aufruft. Der Hostanbieter übergibt den Vorlagenbezeichner des Empfängers im _lpTemplateID_ -Parameter im Aufruf an **IMAPISupport::** opentemplatecollection. MAPI bestimmt, dass der Vorlagenbezeichner zu Ihrem Anbieter gehört, indem der [MAPIUID](mapiuid.md) im Vorlagenbezeichner mit dem **MAPIUID** übereinstimmt, den Ihr Anbieter bei der Anmeldung registriert hat. MAPI leitet dann den Anruf des Host Anbieters über die **IABLogon::** opentemplated-Methode an Ihren Anbieter weiter. 
  
Der Hostanbieter übergibt auch einen Zeiger auf seine Property-Objekt-Implementierung für den Empfänger im _lpMAPIPropData_ -Parameter, einen Schnittstellenbezeichner im _lpInterface_ -Parameter, der dem Typ der Schnittstellenimplementierung entspricht. übergeben in _lpMAPIPropData_und eine optionale Kennzeichnung, FILL_ENTRY. Es wird erwartet, dass Ihr Anbieter im _lppMAPIPropNew_ -Parameter einen Zeiger auf eine Implementierung des Property-Objekts des in _lpInterface_angegebenen Typs zurückgibt. Der zurückgegebene Zeiger kann entweder für das Wrapped Property-Objekt sein, das von Ihrem Anbieter oder für das vom Hostanbieter in _lpMAPIPropData_bereitgestellte Objekt implementiert wurde. Ihr Anbieter sollte einen umschlossenen Property-Objektzeiger zurückgeben, wenn:
  
- Die Anzeigetabelle des Empfängers enthält Listenfeld-Steuerelemente.
    
- Die e-Mail-Adresse des Empfängers muss aus Daten in mehreren Anzeige Tabellen-Steuerelementen zusammengestellt werden.
    
- Der Anbieter gibt Anzeige Tabellen Benachrichtigungen aus.
    
Das FILL_ENTRY-Flag gibt Ihrem Anbieter an, dass der Hostanbieter alle Eigenschaften des Empfängers aktualisieren muss. Der Anbieter muss diese Anforderung erfüllen.
  
Wenn ein Hostanbieter die openTemplate- **** Methode Ihres Anbieters aufruft, kann Ihr Anbieter Folgendes: 
  
- Aktualisieren Sie die Daten für einen kopierten Eintrag regelmäßig.
    
- Halten Sie einen kopierten Eintrag mit seinem Original synchronisiert, beispielsweise wenn ein Adressbucheintrag in das persönliche Adressbuch kopiert wird.
    
- Implementieren Sie Funktionen, die nicht vom Hostanbieter implementiert werden können, wie das dynamische Auffüllen von Listenfeldern in der Details-Tabelle des kopierten Eintrags aus Daten auf einem Server.
    
- Steuern der Interaktion zwischen den Eigenschaften eines kopierten Eintrags oder einer instanziierten Vorlage. Beispiel: Computing **PR_EMAIL_ADDRESS** aus anderen Eigenschaften, die in der Details-Tabelle angezeigt werden. 
    
Die ersten beiden Elemente sind Beispiele für Aufgaben, für die kein Anbieter ein Wrapped Property-Objekt angeben muss – eine Implementierung von **IMAPIProp** , die auf der Implementierung des Host Anbieters basiert. Ihr Anbieter kann die Eigenschaften einfach nach Bedarf aktualisieren und zurückgeben, wobei der _lppMAPIPropNew_ -Parameter so festgelegt wird, dass er auf den vom Hostanbieter im _lpMAPIPropData_ -Parameter übergebenen Zeiger zeigt. 
  
Die zweiten beiden Aufgaben erfordern, dass Ihr Anbieter zum Hostanbieter ein Property-Objekt zurückgibt, das das Objekt des Host Anbieters mit zusätzlicher Funktionalität umschließt, beispielsweise die Möglichkeit, ein Eigenschaftenblatt für den Eintrag anzuzeigen. Dieses Property-Objekt ist entweder ein Messaging-Benutzer oder eine Verteilerliste, je nach Typ des Objekts, das vom Hostanbieter im _lpMAPIPropData_ -Parameter übergeben und durch den Schnittstellenbezeichner im _lpInterface_ -Parameter angegeben wird. Wenn der _lpMAPIPropData_ -Parameter auf einen Messagingbenutzer verweist, muss das Wrapped Property-Objekt des Anbieters eine **IMailUser** -Implementierung sein. Wenn _lpMAPIPropData_ auf eine Verteilerliste verweist, muss es sich um eine **IDistList** -Implementierung handeln. 
  
Das Wrapped Property-Objekt des Anbieters fängt **IMAPIProp** -Methodenaufrufe ab, um die kontextspezifische Manipulation des Empfängers des Host Anbieters zu durchzuführen – das Objekt, das es umfließt. MAPI hat nur eine Anforderung für Wrapped Property Objects: alle Aufrufe an [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , die die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft anfordern, sollten an den Hostanbieter übergeben werden. Die Implementierung Ihres Anbieters kann die zurückgegebene Tabelle verwenden, um Anzeige Tabellen Benachrichtigungen abzufangen oder bei Bedarf eigene hinzuzufügen. 
  
Die folgende Liste enthält Aufgaben, die normalerweise in das von fremden Anbietern implementierte Wrapped Property-Objekt implementiert werden:
  
- Vorverarbeitungs-und postverarbeitungs-Eigenschaftswerte für den Host Empfänger in [IMAPIProp::](imapiprop-getprops.md)GetProps.
    
- Behandlung Details anzeigen von Tabellensteuerelementen wie Schaltflächen und Listenfeldern in **IMAPIProp:: OpenProperty**.
    
- Validieren oder Bearbeiten von Eigenschaftswerten für den Host Empfänger in [IMAPIProp::](imapiprop-setprops.md)SetProps.
    
- Berechnen erforderlicher Eigenschaften wie **PR_EMAIL_ADDRESS** und überprüfen, ob alle erforderlichen Eigenschaften festgelegt wurden, bevor der Host Empfänger in [IMAPIProp:: SaveChanges](imapiprop-savechanges.md)gespeichert wird.
    
### <a name="to-implement-iablogonopentemplateid"></a>So implementieren Sie IABLogon:: openTemplateable
  
1. Überprüfen Sie, ob der mit dem _lpTemplateID_ -Parameter übergebene Vorlagenbezeichner gültig ist und sich in einem Format befindet, das Ihr Anbieter erkennt. Wenn dies nicht der Fall ist, schlagen Sie fehl, und geben Sie MAPI_E_INVALID_ENTRYID. 
    
2. Erstellen Sie ein Objekt des vom Vorlagenbezeichner angegebenen Typs, entweder einen Messagingbenutzer, eine Verteilerliste oder einen einmaligen Empfänger. 
    
3. Rufen Sie die **IUnknown:: AddRef** -Methode im Property-Objekt des Host Anbieters auf, auf das durch den _lpMAPIPropData_ -Parameter verwiesen wird. 
    
4. Wenn der _ulTemplateFlags_ -Parameter auf FILL_ENTRY festgelegt ist: 
    
   1. Wenn es sich bei dem neuen Objekt um einen Messagingbenutzer oder eine Verteilerliste handelt:
      
      1. Rufen Sie alle Eigenschaften des neuen Objekts ab, indem Sie die **IMAPIProp::** GetProps-Methode aufrufen. 
          
      2. Rufen Sie die **IMAPIProp::** SetProps-Methode des Host Anbieters auf, um alle abgerufenen Eigenschaften in das Property-Objekt des Host Anbieters zu kopieren. 
      
   2. Wenn das neue Objekt ein einmaliger Empfänger ist, rufen Sie die **IMAPIProp::** SetProps-Methode des Host Anbieters auf, um die folgenden Eigenschaften festzulegen: 
      
      - **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md)) an den vom Anbieter behandelten Adresstyp.
        
      - **PR\_-Vorlagen** -ID ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md)) zum Vorlagenbezeichner aus den Parametern _lpTemplateID_ und _cbTemplateID_ . 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) an DT_MAILUSER oder DT_DISTLIST.
    
5. Legen Sie den Inhalt des _lppMAPIPropNew_ -Parameters so fest, dass entweder das neue Objekt des Anbieters oder das Property-Objekt, das mit dem _lpMAPIPropData_ -Parameter übergeben wird, angegeben wird, je nachdem, ob Ihr Anbieter ein umschlossenes Objekt bestimmt. 
    
6. Wenn ein kritischer Fehler auftritt, beispielsweise ein Netzwerkfehler oder eine nicht genügend Arbeitsspeicher Bedingung, geben Sie den entsprechenden Fehlerwert zurück. Dieser Wert sollte an den Client mit der entsprechenden [MAPIERROR](mapierror.md) -Struktur weitergegeben werden, eine vom Hostanbieter ausgeführte Aufgabe. 
    

