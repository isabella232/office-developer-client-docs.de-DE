---
title: Suchen des Nachrichtendownloadverlaufs für ein POP3-Konto
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: In diesem Thema wird beschrieben, wie ein e-Mail-Client auf die Pidtagattachdatabinary (-Eigenschaft zugreifen kann, um den Nachrichten Downloadverlauf für ein POP3-Konto abzurufen.
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321875"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Suchen des Nachrichtendownloadverlaufs für ein POP3-Konto

In diesem Thema wird beschrieben, wie ein e-Mail-Client auf die [pidtagattachdatabinary (](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) -Eigenschaft zugreifen kann, um den Nachrichten Downloadverlauf für ein POP3-Konto abzurufen. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Warum soll der Nachrichten Downloadverlauf abgerufen werden?

Der POP-Anbieter (Post Office Protocol) für Outlook ermöglicht Benutzern das Abrufen und Herunterladen neuer e-Mail-Nachrichten auf dem lokalen Gerät und das anschließende verlassen oder Löschen dieser e-Mail-Nachrichten auf dem e-Mail-Server. Wenn der e-Mail-Client prüft, ob neue Nachrichten heruntergeladen werden sollen, muss er nur die neuen Nachrichten für diesen Posteingang identifizieren und herunterladen können. Der e-Mail-Client verwendet dies zunächst mithilfe des UIDL (Unique ID Listing)-Befehls, der eine Zuordnung jeder Nachricht erhält, die jemals an diesen Posteingang an einen eindeutigen Bezeichner (UID) übermittelt wurde. Der Client ruft auch den Nachrichten Downloadverlauf für Nachrichten ab, die heruntergeladen oder für den Posteingang auf diesem Client gelöscht wurden. Mithilfe der Nachrichten-UID-Zuordnung und des downloadverlaufs kann der Client die Nachrichten identifizieren, die im Verlauf als neu vorhanden sind und daher heruntergeladen werden sollten.
  
So rufen Sie den Nachrichten Downloadverlauf für einen Posteingang ab
  
- Führen Sie die Schritte in diesem Thema aus, um die **pidtagattachdatabinary (** -Eigenschaft zu finden, die den Verlauf in einem Binary Large Object (BLOB) enthält, das einem bestimmten Format folgt. 
    
- Lesen Sie weiter mit [dem Analysieren des Nachrichten downloadverlaufs für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md), in dem beschrieben wird, wie Sie dieses BLOB analysieren, um Nachrichten zu identifizieren, die für diesen Posteingang heruntergeladen oder gelöscht wurden.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Kernkonzepte für das Auffinden des Nachrichten downloadverlaufs

Der Nachrichten Downloadverlauf für einen Posteingang wird in einer binären MAPI-Eigenschaft, **pidtagattachdatabinary (**, für eine Anlage einer ausgeblendeten Nachricht im Posteingang gespeichert. In Tabelle 1 sind Ressourcen für Konzepte dargestellt, die Ihnen das Auffinden des Nachrichten downloadverlaufs erleichtern.
  
**Tabelle 1. Kernkonzepte**

|**Titel des Artikels**|**Beschreibung**|
|:-----|:-----|
|[Versteckte MAPI-Ordner](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI ermöglicht es e-Mail-Clients, Informationen in ausgeblendeten Ordnern und ausgeblendeten Nachrichten zu speichern. Versteckte Ordner befinden sich im zugehörigen Teil von MAPI-Ordnern und enthalten in der Regel Informationen, die von Benutzern nicht angezeigt und nicht bearbeitet werden können. Clients entscheiden über das Format und die Inhalte, die in ausgeblendeten Ordnern gespeichert werden sollen.  <br/> |
|[MAPI-Nachrichten](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI speichert Nachrichten in Ordnern, entweder in der standardmäßigen IPM-Unterstruktur, die für Benutzer eines Clients oder außerhalb der Unterstruktur sichtbar ist und für Benutzer unsichtbar ist. Nachrichten können zusätzliche Daten in einer Anlage enthalten, die sich in Form einer Datei, einer anderen Nachricht oder eines OLE-Objekts befinden können. Im Fall des Nachrichten downloadverlaufs wird der Verlauf in einer Eigenschaft einer Nachricht gespeichert, die an eine andere ausgeblendete Nachricht angefügt ist.  <br/> |
|[Übersicht über Nachrichteneigenschaften](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Wenn ein Clientinformationen in einer Nachricht speichert, werden die Informationen tatsächlich in einer Eigenschaft der Nachricht gespeichert. MAPI unterstützt viele Eigenschaften – einige sind immer vorhanden und können von Clients festgelegt werden, andere sind optional – und Clients können nicht erwarten, dass Sie verfügbar oder auf gültige Werte festgelegt werden. Der Nachrichten Downloadverlauf wird in der **pidtagattachdatabinary (** -Eigenschaft einer Anlage einer ausgeblendeten Nachricht gespeichert.  <br/> |
|[MAPI-Profile](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Bei der Anmeldung in einer Sitzung wählt der e-Mail-Client ein Profil aus, das die zu verwendenden Anbieter und Dienste beschreibt. Ein Profil ist in Abschnitte unterteilt, die Eigenschaften enthalten. Insbesondere die Eigenschaften [pidtagsearchkey (](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) und [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) sind immer vorhanden. Der Suchschlüssel eines Profils ist für alle Profile eindeutig und wird im Profil Abschnitt gespeichert, der von **MUID_PROFILE_INSTANCE** (in MAPIGUID definiert ist. H). Verwenden Sie [IMAPISession:: OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) , um den Abschnitt zu öffnen, und verwenden Sie [IMAPIProp::](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) GetProps, um die Eigenschaftswerte abzurufen.  <br/> |
|[Inhaltstabellen](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Nachrichtenspeicher Anbieter implementieren Inhaltstabellen für Ihre Ordner. Bei ausgeblendeten Nachrichten im zugeordneten Teil eines Ordners unterstützen Nachrichtenspeicher Anbieter verknüpfte Inhaltstabellen und Clients können die [IMAPIContainer::](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) getcontentable-Methode verwenden, um einen Zeiger auf die zugeordnete Inhaltstabelle zurückzugeben.  <br/> |
|[Informationen zu Einschränkungen](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Arten von Einschränkungen](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Erstellen einer Einschränkung](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Beispiel für Einschränkungs Code](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |In MAPI können Clients Einschränkungen zum Filtern von Inhaltstabellen verwenden, um nach Zeilen zu suchen, die Nachrichten darstellen, die eine bestimmte Eigenschaft auf einen bestimmten Wert festgelegt haben. Einschränkungen werden mithilfe der [SRestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) -Datenstruktur definiert, die eine Vereinigung spezieller Einschränkungs Strukturen enthalten kann. Die [IMAPITable:: FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) -Methode wendet eine Einschränkung an und ruft die erste Zeile in einer Tabelle ab, die den Einschränkungskriterien entspricht.  <br/> |
|[Informationen zum Registrieren von Speichern für die Indizierung](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Verwenden Sie die [pidtagstoreprovider (](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**)-Eigenschaft, um den Typ des Speicheranbieters zu überprüfen. Um beispielsweise zu überprüfen, ob es sich bei einem Speicher um einen Exchange-Speicher handelt, sollte die **pidtagstoreprovider (** -Eigenschaft einen Wert zurückgeben, der durch die Konstante **pbExchangeProviderPrimaryUserGuid**, die in der öffentlichen Headerdatei edkmdb. h definiert ist.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Auffinden der entsprechenden ausgeblendeten Nachricht und Anlage

Nachdem wir nun wissen, dass sich der Nachrichten Downloadverlauf für einen Posteingang in der **pidtagattachdatabinary (** -Eigenschaft einer Anlage einer ausgeblendeten Nachricht befindet, umfasst die Vorgehensweise zum Auffinden der entsprechenden Anlage der entsprechenden ausgeblendeten Nachricht Folgendes: Verfahren 
  
1. [Suchen der entsprechenden ausgeblendeten Nachricht](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Suchen der entsprechenden Anlage der ausgeblendeten Nachricht](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Zugreifen auf die Pidtagattachdatabinary (-Eigenschaft der Nachrichtenanlage](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Suchen der entsprechenden ausgeblendeten Nachricht

1. Rufen Sie die [pidtagsearchkey (](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**)-Eigenschaft aus dem Profil im durch **MUID_PROFILE_INSTANCE**angegebenen Profil Abschnitt ab.
    
2. Öffnen Sie die zugeordneten Inhalte für den Ordner Posteingang, indem Sie **IMAPIContainer::** getcontentable aufrufen.
    
3. Erstellen Sie eine Einschränkung basierend auf den Eigenschaften [pidtagconversationkey (](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **Pidtagsearchkey (** (**PR_SEARCH_KEY**) und [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**), um eine Tabelle abzurufen, die enthält alle ausgeblendeten Nachrichten in den zugeordneten Inhalten des Posteingangs. Nachfolgend sehen Sie ein Beispiel für eine vom [Auffinden des POP3-UIDL-Verlaufs](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)extrahierte Einschränkung.
    
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

4. Suchen Sie in der Tabelle die ausgeblendete Nachricht mithilfe von **IMAPITable:: FindRow**.
    
5. Wenn in Schritt 4 eine ausgeblendete Nachricht nicht gefunden werden kann, ändern Sie die Einschränkung so, dass **pidtagsearchkey (** (**PR_SEARCH_KEY**) anstelle von **pidtagconversationkey (** verwendet wird (siehe unten):
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Suchen Sie die versteckte Nachricht mit **IMAPITable:: FindRow**. 
    
7. Wenn Schritt 6 fehlschlägt, ändern Sie die Einschränkung so, dass [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_Subject**) mit dem folgenden Wert übereinstimmt ( `printf` siehe unten mithilfe der Format Ersetzung für Kürze). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Suchen Sie die verborgene Nachricht mithilfe von **IMAPITable:: FindRow**.
    
9. Wenn Sie Outlook 2010 oder eine höhere Version ausführen, verwenden Sie die folgenden Werte für **PidTagProfileName** (**PR_PROFILE_NAME**) und **pidtagsearchkey (** (**PR_SEARCH_KEY**).
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Führen Sie die Schritte 3 bis 8 aus. Wenn eine Nachricht nicht gefunden werden kann, greifen Sie auf die ursprünglichen Schritte 3 bis 8 zurück.
    
10. Öffnen Sie die ausgeblendete Nachricht in Schritt 4, 6 oder 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Suchen der entsprechenden Anlage der ausgeblendeten Nachricht

Da die verborgene Nachricht mehr als eine Anlage aufweisen kann, suchen Sie in der folgenden Reihenfolge nach der entsprechenden Anlage.
  
> [!NOTE]
> Bei diesem Verfahren wird erneut `printf` die Format Ersetzung für Kürze verwendet. 

1. Suchen Sie nach einer Anlage, deren [pidtagattachlongfilename (](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) mit der folgenden Zeichen `szEmailAddress` Folge übereinstimmt, wobei die SMTP-Adresse des Benutzers gemäß der Angabe im Profil des Benutzers ist. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Suchen Sie nach einer Anlage, `szEmailAddress`deren [pidtagattachfilename (](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) mit "BlobPOP% s" übereinstimmt.
    
3. Suchen Sie nach einer Anlage, `szEmailAddress`deren [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) mit "BlobPOP% s" übereinstimmt.
    
4. Suchen Sie nach einer Anlage, deren **pidtagattachfilename (** (**PR_ATTACH_FILENAME**) mit "BLOB%. 8X `dwAcctUID`" `dwAcctUID` übereinstimmt, aus [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Sie können die [IOlkAccount:: getprop](iolkaccount-getprop.md) -Methode verwenden, um auf die **PROP_ACCT_MINI_UID** -Eigenschaft zuzugreifen. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Zugreifen auf die Pidtagattachdatabinary (-Eigenschaft der Nachrichtenanlage

Nachdem Sie die entsprechende Nachrichtenanlage der ausgeblendeten Nachricht gefunden haben, verwenden Sie **IMAPIProp::** GetProps, um die **pidtagattachdatabinary (** -Eigenschaft der Anlage zu lesen. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Nächste Schritte

In diesem Thema erfahren Sie, wie Sie den Nachrichten Downloadverlauf für den Posteingang eines POP3-e-Mail-Clients finden. Unter Parsen [des Nachrichten downloadverlaufs für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md) erfahren Sie, wie Sie diesen Verlauf analysieren, um Nachrichten zu identifizieren, die für den Posteingang heruntergeladen oder gelöscht wurden. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>Siehe auch

- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)   
- [Analysieren den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md)
- [Suchen des POP3-UIDL-Verlaufs](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

