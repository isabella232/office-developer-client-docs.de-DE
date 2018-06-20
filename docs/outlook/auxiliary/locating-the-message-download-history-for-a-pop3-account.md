---
title: Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: In diesem Thema wird beschrieben, wie e-Mail-Client die PidTagAttachDataBinary-Eigenschaft zum Abrufen des Nachrichten-Downloadverlauf für ein POP3-Konto zugreifen kann.
ms.openlocfilehash: 00cf5b02e29a22b5165a4aa339230b604722ab6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791117"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto

In diesem Thema wird beschrieben, wie e-Mail-Client die [PidTagAttachDataBinary](http://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) -Eigenschaft zum Abrufen des Nachrichten-Downloadverlauf für ein POP3-Konto zugreifen kann. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Den Nachrichten-Downloadverlauf Warum?

Der Anbieter Post Office Protocol (POP) für Outlook ermöglicht Benutzern abgerufen, und Laden Sie neue e-Mail-Nachrichten auf ihrem lokalen Gerät, und anschließend lassen oder löschen diese e-Mail-Nachrichten auf dem e-Mail-Server. E-Mail-Client für neue Nachrichten herunterladen überprüft, verfügt zu identifizieren, und Laden Sie nur die neuen Nachrichten für Posteingang. E-Mail-Client wird mithilfe von den Befehl UIDL (eindeutige ID aufgelistet), der eine Zuordnung jeder Nachricht abruft, die jemals an Posteingang auf einen eindeutigen Bezeichner (UID) übermittelt wurde. Der Client ruft auch den Nachrichten-Downloadverlauf für Nachrichten, die heruntergeladen oder für den Posteingang auf den Client gelöscht wurden. Mit der Meldung UID-Karte und Downloadverlauf, Identifizieren des Clients kann dann diese Nachrichten, die nicht vorhanden sind im Verlauf als neue und daher sollte heruntergeladen werden.
  
Zum Abrufen des Nachrichten-Downloadverlauf für ein Posteingang:
  
- Führen Sie die Schritte in diesem Thema, um die Eigenschaft **PidTagAttachDataBinary** zu finden, die den Verlauf in ein binary large Object (BLOB) enthält, die ein bestimmtes Format folgt. 
    
- Fahren Sie mit der [Analyse den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md), das beschreibt das Analysieren dieser BLOB, um Nachrichten zu ermitteln, die heruntergeladen oder für Posteingang gelöscht wurden.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Kernkonzepte für die Suche nach der Nachricht Downloadverlauf

Der Nachricht Downloadverlauf für einen Posteingang wird in eine binäre MAPI-Eigenschaft, **PidTagAttachDataBinary**, für eine Anlage einer ausgeblendete Nachricht im Posteingang gespeichert. Tabelle 1 zeigt die Ressourcen für die Konzepte, erläutert, wie Sie die Nachricht suchen Chatverlauf herunterzuladen.
  
**In Tabelle 1. Zentrale Konzepte**

|**Titel des Artikels**|**Beschreibung**|
|:-----|:-----|
|[MAPI-ausgeblendet Ordner](http://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI ermöglicht es e-Mail-Clients zum Speichern von Informationen in ausgeblendeten Ordnern und ausgeblendete Nachrichten. Verborgene Ordner befinden sich in der zugeordneten Teil des MAPI-Ordner und in der Regel enthalten Informationen, die nicht sichtbar sind und nicht durch Benutzer geändert werden. Clients entscheiden, das Format und der Inhalt im ausgeblendete Nachrichten in verborgene Ordner speichern.  <br/> |
|[MAPI-Nachrichten](http://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI werden Nachrichten gespeichert, in Ordnern, entweder in der standard-IPM-Unterstruktur, die für Benutzer von einem Client oder außerhalb der Unterstruktur und für den Benutzer unsichtbar sichtbar ist. Nachrichten können zusätzliche Daten in einer Anlage, die in Form einer Datei, eine andere Nachricht oder ein OLE-Objekt sein kann gespeichert haben. Bei der Nachrichten-Downloadverlauf wird der Verlauf in einer Eigenschaft einer Nachricht gespeichert, die an eine andere ausgeblendete Nachricht angefügt wird.  <br/> |
|[Nachricht Eigenschaften (Übersicht)](http://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Wenn ein Client Informationen in einer Nachricht speichert, speichert es tatsächlich die Informationen in einer Eigenschaft der Nachricht an. MAPI unterstützt viele Eigenschaften – einige immer vorhanden und kann von Clients festgelegt werden, andere sind optional – und Clients können nicht erwarten, dass sie verfügbar oder festgelegt werden, gültige Werte. Der Nachrichten-Downloadverlauf wird in der **PidTagAttachDataBinary** -Eigenschaft auf eine ausgeblendete Nachricht einer Anlage gespeichert.  <br/> |
|[MAPI-Profile](http://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Bei der Anmeldung in einer Sitzung wählt der e-Mail-Client ein Profil, das den Anbieter und die Dienste zu verwendende beschreibt. Ein Profil ist in Abschnitte unterteilt, die Eigenschaften enthalten. Insbesondere die [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) und [PidTagProfileName](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) Eigenschaften sind immer vorhanden. Ein Profil Search-Schlüssel ist eindeutig für alle Profile, und befindet sich im Profilabschnitt, der von **MUID_PROFILE_INSTANCE** angegeben wird (die im MAPIGUID definiert ist. H). Verwenden Sie [IMAPISession::OpenProfileSection](http://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) , um den Abschnitt zu öffnen, und verwenden Sie [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) , um die Eigenschaftswerte abzurufen.  <br/> |
|[Inhalt von Tabellen](http://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Nachricht Anbieter implementieren Inhalt Tabellen für ihre Ordner. Ausgeblendete Nachrichten in das zugeordnete Teil eines Ordners Nachricht Anbieter unterstützen zugeordneten Inhalt Tabellen und Clients können die [IMAPIContainer::GetContentsTable](http://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) -Methode verwenden, um einen Zeiger auf die Inhaltstabelle zugeordneten zurückzugeben.  <br/> |
|[Informationen zu Einschränkungen](http://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Arten von Einschränkungen](http://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Erstellen eine Einschränkung](http://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Beispielcode für die Einschränkung](http://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |In MAPI können Clients Einschränkungen zum Filtern von Inhalt Tabellen, Zeilen suchen, die Nachrichten darstellen, die eine bestimmte Eigenschaft auf einen bestimmten Wert festgelegt haben. Einschränkungen werden mithilfe der [SRestriction](http://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) -Datenstruktur, die eine Vereinigung von speziellere Einschränkung Strukturen enthalten kann definiert. Die [IMAPITable](http://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) -Methode wendet die Einschränkung an und ruft die erste Zeile in einer Tabelle, die die Einschränkungskriterien entspricht.  <br/> |
|[Zum Registrieren von Speicher für die Indizierung](http://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Verwenden Sie die [PidTagStoreProvider](http://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**)-Eigenschaft, um den Typ des Anbieters sicherzustellen. Beispielsweise sollte um zu überprüfen, ob ein Speicher einen Exchange-Speicher ist, die **PidTagStoreProvider** -Eigenschaft einen Wert zurückgeben, dargestellt durch die Konstante **PbExchangeProviderPrimaryUserGuid**, die in der öffentlichen Header-Datei edkmdb.h definiert ist.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Suchen nach den entsprechenden ausgeblendete Nachricht und Anlage

Nun, wir, dass der Nachricht Downloadverlauf für einen Posteingang in der **PidTagAttachDataBinary** -Eigenschaft auf eine ausgeblendete Nachricht einer Anlage ist wissen, umfasst die Vorgehensweise zum Suchen nach der entsprechenden Anlage der entsprechenden ausgeblendete Nachricht Folgendes Verfahren: 
  
1. [Suchen Sie nach der entsprechenden ausgeblendete Nachricht](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Suchen Sie nach der entsprechenden Anlage der ausgeblendete Nachricht](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Zugriff auf die PidTagAttachDataBinary-Eigenschaft des e-Mail-Nachrichtenanhang](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Suchen Sie nach der entsprechenden ausgeblendete Nachricht

1. Rufen Sie die Eigenschaft [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) aus dem Profil im Profilabschnitt durch **MUID_PROFILE_INSTANCE**angegeben.
    
2. Öffnen Sie den Inhalt verknüpft ist, für den Ordner Posteingang durch Aufrufen von **IMAPIContainer::GetContentsTable**.
    
3. Erstellen Sie eine Einschränkung basierend auf der [PidTagConversationKey](http://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**PR_SEARCH_KEY**) und [PidTagMessageClass](http://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) Eigenschaften zum Abrufen einer Tabelle, enthält alle ausgeblendeten Nachrichten im Inhalt des Posteingangs verknüpft ist. Es folgt ein Beispiel für eine Einschränkung finden Sie [Den POP3 UIDL Verlauf](http://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)extrahiert haben.
    
   ```cpp
      SRestriction rgRes[3]; 
      SPropValue rgProps[3]; 
      rgRes[0].rt = RES_AND; 
      rgRes[0].res.resAnd.cRes = 2; 
      rgRes[0].res.resAnd.lpRes = &amp;rgRes[1]; 
      rgRes[1].rt = RES_PROPERTY; 
      rgRes[1].res.resProperty.relop = RELOP_EQ; 
      rgRes[1].res.resProperty.ulPropTag = PR_CONVERSATION_KEY; 
      rgRes[1].res.resProperty.lpProp = &amp;rgProps[0]; 
      rgRes[2].rt = RES_PROPERTY; 
      rgRes[2].res.resProperty.relop = RELOP_EQ; 
      rgRes[2].res.resProperty.ulPropTag = PR_MESSAGE_CLASS; 
      rgRes[2].res.resProperty.lpProp = &amp;rgProps[1]; 
      rgProps[0].ulPropTag = PR_CONVERSATION_KEY; 
      rgProps[0].Value.bin = pVals[iSearchKey].Value.bin; // PR_SEARCH_KEY from the profile 
      rgProps[1].ulPropTag = PR_MESSAGE_CLASS; 
      rgProps[1].Value.LPSZ = (LPTSTR)"IPM.MessageManager";
   ```

4. Hier finden Sie ausgeblendete Nachricht mithilfe von **IMAPITable**, aus der Tabelle.
    
5. Wenn Schritt 4 fehlschlägt, ausgeblendete Nachricht zu erhalten, ändern Sie die Einschränkung zu **PidTagSearchKey** (**PR_SEARCH_KEY**) anstelle von **PidTagConversationKey**, verwenden Sie wie folgt:
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Hier finden Sie die ausgeblendete Nachricht **IMAPITable**verwenden. 
    
7. Wenn Schritt 6 ein Fehler auftritt, ändern Sie die Einschränkung zu [PidTagSubject](http://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) wird auf den folgenden Wert verwenden (wie unten gezeigt verwenden `printf` Ersetzung der Kürze halber formatieren). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Suchen Sie ausgeblendete Nachricht mithilfe von **IMAPITable**.
    
9. Wenn Sie Outlook 2010 oder eine höhere Version ausgeführt werden, verwenden Sie jeweils die folgenden Werte für **PidTagProfileName** (**PR_PROFILE_NAME**) und **PidTagSearchKey** (**PR_SEARCH_KEY**).
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Führen Sie die Schritte 3 bis 8. Wenn dies fehlschlägt, eine Nachricht zu erhalten, zurückgreifen Sie auf die ursprüngliche Schritte 3 bis 8.
    
10. Öffnen Sie die ausgeblendete Nachricht in Schritt 4, 6 oder 8 gefunden wurde.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Suchen Sie nach der entsprechenden Anlage der ausgeblendete Nachricht

Da ausgeblendete Nachricht mehr als eine Anlage möglicherweise, suchen Sie nach der entsprechenden Anlage in der folgenden Reihenfolge.
  
> [!NOTE]
> Dieses Verfahren erneut verwendet die `printf` Ersetzung der Kürze halber formatieren. 

1. Suchen Sie nach einer Anlage, deren [PidTagAttachLongFilename](http://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) die folgende Zeichenfolge übereinstimmt, in dem `szEmailAddress` SMTP-Adresse des Benutzers, wie im Profil des Benutzers angegeben ist. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Suchen Sie nach einer Anlage, deren [PidTagAttachFilename](http://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) entspricht "BlobPOP %s" `szEmailAddress`.
    
3. Suchen Sie nach einer Anlage, deren [PidTagDisplayName](http://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) entspricht "BlobPOP %s" `szEmailAddress`.
    
4. Suchen Sie nach einer Anlage, deren **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) entspricht "Blob%.8x", `dwAcctUID`, wobei `dwAcctUID` [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md)stammt. Die [IOlkAccount::GetProp](iolkaccount-getprop.md) -Methode können Sie die **PROP_ACCT_MINI_UID** -Eigenschaft zugreifen. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Zugriff auf die PidTagAttachDataBinary-Eigenschaft des e-Mail-Nachrichtenanhang

Verwenden Sie nach der Suche nach den entsprechenden e-Mail-Nachrichtenanhang der ausgeblendete Nachricht, **IMAPIProp::GetProps** , um die **PidTagAttachDataBinary** -Eigenschaft der Anlage zu lesen. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Nächste Schritte

Sie haben zum Ermitteln den Nachrichten-Downloadverlauf für den Posteingang von POP3 e-Mail-Client in diesem Thema erfahren. Finden Sie unter [analysieren den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md) , um Informationen zum Analysieren der Verlauf, um Nachrichten zu ermitteln, die heruntergeladen oder für den Posteingang gelöscht wurden. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>Siehe auch

- [Verwalten von Nachricht downloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)   
- [Analysieren den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md)
- [Suchen den POP3 UIDL-Verlauf](http://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

