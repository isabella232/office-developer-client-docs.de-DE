---
title: Fungiert als eine foreign-Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cafc6e3b6d863a7c2acec5811bf161ad0cd64458
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570030"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Fungiert als eine foreign-Adressbuchanbieter

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Fremdschlüssel Anbieter ist Adressbuch-Dienstanbieter, die: 
  
- Weist Vorlage-IDs für die Empfänger an.
    
- Unterstützt die [OpenTemplateID](iablogon-opentemplateid.md) -Methode. 
    
- Stellt Code für die Verwaltung von Empfängern an, die im Container der anderen adressbuchanbietern implementierte bekannt als Hostanbieter vorhanden sein. Dieser Code umfasst ein Property-Objekt, in der Regel eine **IMAPIProp** Implementierung, die ein Property-Objekt aus der Hostanbieter umschließt. 
    
Als fremden Anbieter fungiert, ist eine optionale Rolle. nicht alle Anbieter müssen Vorlage-IDs und ihre zugehörigen Code unterstützen. Implementieren Sie einen Anbieter als fremden Anbieter, wenn Sie möchten Kontrolle über Empfänger zu verwalten, die Hostanbieter Erstellen von Vorlagen, die von Ihrem Anbieter bereitgestellt wird. 
  
Das Format, das vom Dienstanbieter für ihre Eintragsbezeichner verwendet wird, kann auch für ihre Vorlage Bezeichner verwendet werden. Vorlage Bezeichner müssen Ihres Anbieters registrierten **MAPIUID** zum Aktivieren von MAPI Empfänger erfolgreich an den entsprechenden Anbietern binden enthalten. 
  
MAPI-Aufrufen des Anbieters **OpenTemplateID** -Methode, wenn ein Host-Aufrufe eines [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). Hostanbieter übergibt den Vorlagenbezeichner des Empfängers im _LpTemplateID_ -Parameter in dem Aufruf von **IMAPISupport::OpenTemplateID**. MAPI bestimmt, dass die Vorlage-ID an Ihren Anbieter durch entsprechende [MAPIUID](mapiuid.md) in der Vorlagenbezeichner mit der **MAPIUID** , die bei der Anmeldung vom Dienstanbieter registriert gehört. MAPI leitet dann die Hostanbieter Aufruf an Ihren Anbieter der **OpenTemplateID** -Methode. 
  
Hostanbieter übergibt außerdem einen Zeiger auf die Implementierung der Eigenschaft-Objekt für den Empfänger im Parameter _LpMAPIPropData_ , ein Schnittstellenbezeichner in der _LpInterface_ -Parameter, der den Typ des schnittstellenimplementierung entspricht in _LpMAPIPropData_und eine optionale Kennzeichnung, FILL_ENTRY übergeben. Wird erwartet, dass der Anbieter in der _LppMAPIPropNew_ -Parameter einen Zeiger auf eine Implementierung der Eigenschaft-Objekt vom Typ in _LpInterface_zurückzugeben. Der zurückgegebene Zeiger kann entweder von Ihrem Anbieter implementiert gepackten Property-Objekt oder das Objekt, das vom Host Provider in _LpMAPIPropData_sein. Der Anbieter sollte einen Zeiger des eingebundenen Eigenschaft-Objekt zurückgeben wenn:
  
- Zeigt die Tabelle des Empfängers enthält Listenfeld-Steuerelemente.
    
- Anhand von Daten in mehrere Anzeige Tabellensteuerelemente muss die e-Mail-Adresse für den Empfänger zusammengestellt werden.
    
- Ihre Anbieter Probleme anzeigen Tabelle Benachrichtigungen
    
Das Flag FILL_ENTRY zeigt Ihres Anbieters Hostanbieter alle Eigenschaften des Empfängers zu aktualisierenden erforderlich ist. Der Anbieter ist erforderlich, zur Erfüllung dieser Anforderung.
  
Wenn ein Hostanbieter Ihres Anbieters **OpenTemplateID** -Methode aufgerufen wird, kann vom Dienstanbieter: 
  
- Aktualisieren Sie die Daten in einem Eintrag der kopierten regelmäßig.
    
- Lassen Sie einen kopierten Eintrag mit den ursprünglichen, beispielsweise wenn ein Buch Adresseintrag in das persönliche Adressbuch kopiert wird synchronisiert.
    
- Felder in den kopierten Eintrag Detailtabelle anhand von Daten auf einem Server wird implementieren-Funktionen, die vom Hostanbieter wie dynamisches Auffüllen der Liste nicht implementiert werden kann.
    
- Steuern der Interaktion zwischen Eigenschaften in einem kopierten Eintrag oder instanziierten Vorlage. Beispielsweise computing **PR_EMAIL_ADDRESS** von anderen Eigenschaften in der Detailtabelle angezeigt. 
    
Die ersten beiden Elemente sind Beispiele für Aufgaben, die vom Dienstanbieter bereitstellen ein gepackten Property-Objekt keine erfordern – eine Implementierung der **IMAPIProp** , die auf die Hostanbieter Implementierung basiert. Vom Dienstanbieter kann einfach die Eigenschaften wie erforderlich und zurückgegeben, wenn der _LppMAPIPropNew_ -Parameter vom Hostanbieter im _LpMAPIPropData_ -Parameter übergebene Zeiger auf aktualisieren. 
  
Die nächsten zwei Aufgaben erfordern, dass der Anbieter für den Hostanbieter ein Property-Objekt zurückgeben, der den Hostanbieter-Objekt mit zusätzlichen Funktionen, wie etwa die Möglichkeit zum Anzeigen von einem Eigenschaftenfenster für den Eintrag umbrochen wird. Diese Property-Objekt wird entweder ein messaging Benutzer oder Verteilerliste aus, je nach den Typ des Objekts vom Hostanbieter im _LpMAPIPropData_ -Parameter übergeben und von der Schnittstelle-ID in der _LpInterface_ -Parameter angegeben werden. Wenn der Parameter _LpMAPIPropData_ auf ein messaging-Benutzer zeigt, muss Ihres Anbieters gepackten Property-Objekt eine Implementierung **IMailUser** sein. Wenn _LpMAPIPropData_ an eine Verteilerliste verweist, muss es sich eine Implementierung **IDistList** handeln. 
  
Ihres Anbieters gepackten Property-Objekt fängt **IMAPIProp** -Methodenaufrufe, kontextabhängige Bearbeitung der Empfänger die Hostanbieter auszuführen – das Objekt er umbrochen wird. MAPI hat nur eine Anforderung für umbrochenen Property-Objekte: alle Aufrufe von [IMAPIProp::OpenProperty](imapiprop-openproperty.md) Anfordern der **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft für den Hostanbieter übergeben werden sollte. Der Implementierung des Anbieters können die zurückgegebene Tabelle zum Abfangen von anzeigebenachrichtigungen Tabelle oder eine eigene bei Bedarf hinzuzufügen. 
  
Die folgende Liste enthält die Aufgaben, die in der Regel in von fremden Anbietern implementiert gepackten Property-Objekt implementiert werden:
  
- Der vorverarbeitung und Eigenschaftswerte für den Host Empfänger in [IMAPIProp::GetProps](imapiprop-getprops.md)Traditionsgemäß.
    
- Behandlung Details anzeigen Table-Steuerelemente, wie Schaltflächen und Listenfelder, **IMAPIProp::OpenProperty**
    
- Überprüfen oder Ändern von Eigenschaftswerten für den Host Empfänger in [IMAPIProp::SetProps](imapiprop-setprops.md).
    
- Erforderliche Eigenschaften wie **PR_EMAIL_ADDRESS** Computing und sicherstellen, dass alle erforderlichen Eigenschaften vor dem Speichern des Host-Empfängers in [IMAPIProp::SaveChanges](imapiprop-savechanges.md)festgelegt wurden.
    
### <a name="to-implement-iablogonopentemplateid"></a>OpenTemplateID implementieren
  
1. Überprüfen Sie, wenn der Vorlagenbezeichner mit übergeben der _LpTemplateID_ -Parameter ist gültig und befindet sich in einem Format, das Ihren Anbieter erkennt. Wenn sie nicht der Fall ist, ein Fehler auftritt, und geben Sie MAPI_E_INVALID_ENTRYID zurück. 
    
2. Erstellen Sie ein Objekt vom Typ angegeben durch den Vorlagenbezeichner messaging-Benutzer, Verteilerliste oder einmal-Empfänger. 
    
3. Rufen Sie die **IUnknown:: AddRef** -Methode in der Hostanbieter Property-Objekt das Objekt ist, durch den Parameter _LpMAPIPropData_ auf. 
    
4. Wenn der Parameter _UlTemplateFlags_ auf FILL_ENTRY festgelegt ist: 
    
   1. Wenn das neue Objekt eine messaging Liste Benutzer oder eine Verteilergruppe ist:
      
      1. Rufen Sie aller Eigenschaften des neuen Objekts ab, möglicherweise durch seine **IMAPIProp::GetProps** -Methode aufrufen. 
          
      2. Rufen Sie die Hostanbieter **IMAPIProp::SetProps** -Methode, um alle abgerufenen Eigenschaften auf die Hostanbieter Property-Objekt zu kopieren. 
      
   2. Wenn das neue Objekt einen einmaligen Empfänger ist, rufen Sie die Hostanbieter **IMAPIProp::SetProps** -Methode, um die folgenden Eigenschaften festlegen: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) vom Anbieter für den Adresstyp behandelt.
        
      - **Kurs\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) auf die Vorlagenbezeichner der Parameter _LpTemplateID_ und _CbTemplateID_ . 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER oder DT_DISTLIST, je nach Bedarf.
    
5. Legen Sie den Inhalt des Parameters _LppMAPIPropNew_ , zeigen Sie auf Neues Objekt Ihres Anbieters oder Property-Objekt übergeben wird, sich mit der _LpMAPIPropData_ -Parameter, je nachdem, ob vom Dienstanbieter wird bestimmt, ob ein gepackten Objekt erforderlich ist. 
    
6. Den entsprechende Fehlermeldung-Wert zurück, wenn ein schwerwiegender Fehler, wie ein Netzwerkfehler oder nicht genügend Arbeitsspeicher verfügt auftritt. Dieser Wert sollte an den Client mit der entsprechenden [MAPIERROR](mapierror.md) -Struktur eines Vorgangs durchgeführt vom Hostanbieter weitergegeben werden. 
    

