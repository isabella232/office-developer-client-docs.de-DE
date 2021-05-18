---
title: Suchen des Nachrichtendownloadverlaufs für ein POP3-Konto
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: 'In diesem Thema wird beschrieben, wie ein E-Mail-Client auf die PidTagAttachDataBinary-Eigenschaft zugreifen kann, um den Nachrichtendownloadverlauf für ein #A0 zu erhalten.'
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321875"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Suchen des Nachrichtendownloadverlaufs für ein POP3-Konto

In diesem Thema wird beschrieben, wie ein E-Mail-Client auf die [PidTagAttachDataBinary-Eigenschaft](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) zugreifen kann, um den Nachrichtendownloadverlauf für ein #A0 zu erhalten. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Warum den Nachrichtendownloadverlauf erhalten?

Der Post Office Protocol (POP)-Anbieter für Outlook ermöglicht Benutzern das Abrufen und Herunterladen neuer E-Mail-Nachrichten auf ihrem lokalen Gerät und anschließend das Verlassen oder Löschen dieser E-Mail-Nachrichten auf dem E-Mail-Server. Wenn der E-Mail-Client überprüft, ob neue Nachrichten heruntergeladen werden sollen, muss er nur die neuen Nachrichten für diesen Posteingang identifizieren und herunterladen können. Der E-Mail-Client verwendet dazu zunächst den Befehl UIDL (Unique ID Listing), der eine Karte jeder Nachricht erhält, die jemals an diesen Posteingang an einen eindeutigen Bezeichner (Unique Identifier, UID) zugestellt wurde. Der Client ruft außerdem den Nachrichtendownloadverlauf für Nachrichten ab, die für den Posteingang auf diesem Client heruntergeladen oder gelöscht wurden. Mithilfe der UiD-Karte und des Downloadverlaufs der Nachricht kann der Client dann die Nachrichten identifizieren, die im Verlauf nicht vorhanden sind, als neu und sollten daher heruntergeladen werden.
  
So erhalten Sie den Nachrichtendownloadverlauf für einen Posteingang:
  
- Führen Sie die Schritte in diesem Thema aus, um die **PidTagAttachDataBinary-Eigenschaft** zu finden, die den Verlauf in einem binary large object (BLOB) enthält, das einem bestimmten Format folgt. 
    
- Fahren Sie mit der Analyse des Nachrichtendownloadverlaufs für ein [POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md)fort, in dem beschrieben wird, wie dieser BLOB analysiert wird, um Nachrichten zu identifizieren, die für diesen Posteingang heruntergeladen oder gelöscht wurden.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Kernkonzepte zum Suchen des Nachrichtendownloadverlaufs

Der Nachrichtendownloadverlauf für einen Posteingang wird in der binären #A0 **PidTagAttachDataBinary** in einer Anlage einer ausgeblendeten Nachricht im Posteingang gespeichert. Tabelle 1 enthält Ressourcen für Konzepte, mit deren Hilfe Sie den Nachrichtendownloadverlauf ermitteln können.
  
**Tabelle 1. Kernkonzepte**

|**Titel des Artikels**|**Beschreibung**|
|:-----|:-----|
|[MAPI Ausgeblendete Ordner](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI ermöglicht E-Mail-Clients das Speichern von Informationen in ausgeblendeten Ordnern und ausgeblendeten Nachrichten. Ausgeblendete Ordner befinden sich im zugeordneten Teil von MAPI-Ordnern und enthalten in der Regel Informationen, die für Benutzer nicht sichtbar sind und nicht von Benutzern bearbeitet werden sollen. Clients entscheiden, welche Formate und Inhalte in ausgeblendeten Nachrichten in ausgeblendeten Ordnern gespeichert werden sollen.  <br/> |
|[MAPI-Nachrichten](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI speichert Nachrichten in Ordnern, entweder in der standardmäßigen IPM-Unterstruktur, die für Benutzer eines Clients sichtbar ist, oder außerhalb der Unterstruktur und unsichtbar für Benutzer. Nachrichten können zusätzliche Daten in einer Anlage gespeichert haben, die in Form einer Datei, einer anderen Nachricht oder eines OLE-Objekts sein können. Im Fall des Nachrichtendownloadverlaufs wird der Verlauf in einer Eigenschaft einer Nachricht gespeichert, die an eine andere ausgeblendete Nachricht angefügt ist.  <br/> |
|[Übersicht über Nachrichteneigenschaften](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Wenn ein Client Informationen in einer Nachricht speichert, speichert er die Informationen tatsächlich in einer Eigenschaft der Nachricht. MAPI unterstützt viele Eigenschaften – einige sind immer vorhanden und können von Clients festgelegt werden, andere sind optional – und Clients können nicht erwarten, dass sie verfügbar sind oder auf gültige Werte festgelegt werden. Der Nachrichtendownloadverlauf wird in der **PidTagAttachDataBinary-Eigenschaft** einer Anlage mit einer ausgeblendeten Nachricht gespeichert.  <br/> |
|[MAPI-Profile](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Bei der Anmeldung in einer Sitzung wählt der E-Mail-Client ein Profil aus, das die zu verwendenden Anbieter und Dienste beschreibt. Ein Profil ist in Abschnitte unterteilt, die Eigenschaften enthalten. Insbesondere die [Eigenschaften PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) und [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) sind immer vorhanden. Der Suchschlüssel eines Profils ist unter allen Profilen eindeutig und wird im Profilabschnitt gespeichert, der von MUID_PROFILE_INSTANCE **(in** MAPIGUID definiert) identifiziert wird. H). Verwenden [Sie IMAPISession::OpenProfileSection,](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) um den Abschnitt zu öffnen, und verwenden [Sie IMAPIProp::GetProps,](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) um die Eigenschaftswerte zu erhalten.  <br/> |
|[Inhaltstabellen](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Nachrichtenspeicheranbieter implementieren Inhaltstabellen für ihre Ordner. Bei ausgeblendeten Nachrichten im zugeordneten Teil eines Ordners unterstützen Nachrichtenspeicheranbieter tabellen zugeordnete Inhaltstabellen, und Clients können die [IMAPIContainer::GetContentsTable-Methode](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) verwenden, um einen Zeiger auf die zugeordnete Inhaltstabelle zurückzukehren.  <br/> |
|[Informationen zu Einschränkungen](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Arten von Einschränkungen](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Erstellen einer Einschränkung](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Beispieleinschränkungscode](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |In MAPI können Clients Einschränkungen verwenden, um Inhaltstabellen zu filtern und nach Zeilen zu suchen, die Nachrichten darstellen, für die eine bestimmte Eigenschaft auf einen bestimmten Wert festgelegt ist. Einschränkungen werden mithilfe der [SRestriction-Datenstruktur](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) definiert, die eine Vereinigung speziellerer Einschränkungsstrukturen enthalten kann. Die [IMAPITable::FindRow-Methode](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) wendet eine Einschränkung an und ruft die erste Zeile in einer Tabelle ab, die den Einschränkungskriterien entspricht.  <br/> |
|[Informationen zum Registrieren von Informationsspeichern für die Indizierung](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Verwenden Sie [die PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) -Eigenschaft, um den Typ des Speicheranbieters zu überprüfen. Um beispielsweise zu überprüfen, ob es sich bei einem Speicher um einen Exchange-Speicher handelt, sollte die **PidTagStoreProvider-Eigenschaft** einen Wert zurückgeben, der durch die Konstante **pbExchangeProviderPrimaryUserGuid** dargestellt wird, die in der öffentlichen Headerdatei edkmdb.h definiert ist.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Suchen der entsprechenden ausgeblendeten Nachricht und Anlage

Da wir nun wissen, dass sich der Nachrichtendownloadverlauf für einen Posteingang in der **PidTagAttachDataBinary-Eigenschaft** einer Anlage zu einer ausgeblendeten Nachricht befindet, umfasst das Verfahren zum Suchen der entsprechenden Anlage der entsprechenden ausgeblendeten Nachricht die folgenden Verfahren: 
  
1. [Suchen der entsprechenden ausgeblendeten Nachricht](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Suchen der entsprechenden Anlage der ausgeblendeten Nachricht](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Zugreifen auf die PidTagAttachDataBinary-Eigenschaft der Nachrichtenanlage](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Suchen der entsprechenden ausgeblendeten Nachricht

1. Get the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) property from the profile, in the profile section specified by **MUID_PROFILE_INSTANCE**.
    
2. Öffnen Sie den Zugeordneten Inhalt für den Ordner Posteingang, indem Sie **IMAPIContainer::GetContentsTable aufrufen.**
    
3. Erstellen Sie eine Einschränkung basierend auf den Eigenschaften [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**PR_SEARCH_KEY**) und [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**), um eine Tabelle zu erhalten, die alle ausgeblendeten Nachrichten im Zugeordneten Inhalt des Posteingangs enthält. Im Folgenden finden Sie ein Beispiel für eine Einschränkung, die aus der Suche nach dem [POP3-UIDL-Verlauf extrahiert wurde.](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    
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

4. Suchen Sie in der Tabelle die ausgeblendete Nachricht mithilfe von **IMAPITable::FindRow**.
    
5. Wenn in Schritt 4 keine ausgeblendete Nachricht zu finden ist, ändern Sie die Einschränkung so, dass **PidTagSearchKey** (**PR_SEARCH_KEY**) anstelle von **PidTagConversationKey** verwendet wird, wie unten gezeigt:
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Suchen Sie die ausgeblendete Nachricht mithilfe **von IMAPITable::FindRow**. 
    
7. Wenn In Schritt 6 ein Fehler auftritt, ändern Sie die Einschränkung so, dass [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) dem folgenden Wert entspricht (siehe unten mit Formatersetzung für  `printf` Kürze). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Suchen Sie die ausgeblendete Nachricht mithilfe von **IMAPITable::FindRow**.
    
9. Wenn Sie Outlook 2010 oder höher ausführen, verwenden Sie die folgenden Werte für **PidTagProfileName** (**PR_PROFILE_NAME**) **bzw. PidTagSearchKey** (**PR_SEARCH_KEY**).
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Führen Sie die Schritte 3 bis 8 aus. Wenn dadurch keine Nachricht angezeigt wird, können Sie auf die ursprünglichen Schritte 3 bis 8 zurückfallen.
    
10. Öffnen Sie die ausgeblendete Nachricht in Schritt 4, 6 oder 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Suchen der entsprechenden Anlage der ausgeblendeten Nachricht

Da die ausgeblendete Nachricht möglicherweise mehrere Anlagen enthält, suchen Sie in der folgenden Reihenfolge nach der entsprechenden Anlage.
  
> [!NOTE]
> In diesem Verfahren wird erneut die  `printf` Formatvorlage als Ersatz für Kürze verwendet. 

1. Suchen Sie nach einer Anlage, deren [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) der folgenden Zeichenfolge entspricht, wobei die #A0 des Benutzers ist, wie im Benutzerprofil  `szEmailAddress` angegeben. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Suchen Sie nach einer Anlage, deren [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) "BlobPOP%s",  `szEmailAddress` entspricht.
    
3. Suchen Sie nach einer Anlage, deren [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) "BlobPOP%s" entspricht,  `szEmailAddress` .
    
4. Suchen Sie nach einer Anlage, deren **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) "Blob%.8x" entspricht, wobei aus `dwAcctUID` `dwAcctUID` PROP_ACCT_MINI_UID. [](prop_acct_mini_uid.md) Sie können die [IOlkAccount::GetProp-Methode](iolkaccount-getprop.md) verwenden, um auf die **PROP_ACCT_MINI_UID** zugreifen. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Zugreifen auf die PidTagAttachDataBinary-Eigenschaft der Nachrichtenanlage

Verwenden Sie nach dem Suchen der entsprechenden Nachrichtenanlage der ausgeblendeten Nachricht **IMAPIProp::GetProps,** um die **PidTagAttachDataBinary-Eigenschaft** der Anlage zu lesen. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Nächste Schritte

Sie haben aus diesem Thema gelernt, wie Sie den Nachrichtendownloadverlauf für den Posteingang eines POP3-E-Mail-Clients finden. Unter Analysieren des Nachrichtendownloadverlaufs für ein [POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md) erfahren Sie, wie Sie diesen Verlauf analysieren, um Nachrichten zu identifizieren, die für den Posteingang heruntergeladen oder gelöscht wurden. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)   
- [Analysieren den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md)
- [Suchen des POP3-UIDL-Verlaufs](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

