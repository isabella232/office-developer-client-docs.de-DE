---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8d7e6dfbf9e6a751845adb2319b66462bcde651f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792095"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**Betrifft**: Outlook 
  
Erstellt eine neue Nachricht an.
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle, greifen Sie auf die neue Nachricht verwendet werden soll. Gültige Schnittstelle Bezeichnern enthalten IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder. Übergeben von NULL wird eine Nachricht an die e-Mail-Schnittstelle zurück, die [IMessage: IMAPIProp](imessageimapiprop.md). 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Nachricht erstellt wird. Die folgenden Kennzeichen können festgelegt werden:
    
ITEMPROC_FORCE
  
> Gibt an, dass die Nachricht für Informationsspeicher für Persönliche Ordner (PST) Regeln verarbeiten, bevor der Speicher jeder listening Client die Ankunft der neuen Nachricht informiert. Nur regelverarbeitung gilt für neue Nachrichten, die auf einem Server, der nicht auf einem Microsoft Exchange Server ist erstellt werden, da Exchange Server Regeln für Nachrichten auf dem Server verarbeitet. Aus diesem Grund muss vom Anbieter oder vom Client beim Erstellen der Nachricht übergeben dieses Flag in Kombination mit dem Speichern einer Nachricht mit [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) mit NON_EMS_XP_SAVE, die angibt, dass der Server nicht mit einem Exchange-Server ist. 
    
MAPI_ASSOCIATED 
  
> Die Nachricht zu erstellenden sollte in der zugehörigen Inhaltstabelle anstelle der standard Inhaltstabelle enthalten sein. Benutzerinteraktion werden zugeordnete Nachrichten ausgeblendet.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** darf erfolgreich, auch wenn der Vorgang zum Erstellen eines nicht vollständig ausgeführt wurde. Dies bedeutet, dass die neue Nachricht möglicherweise nicht sofort mit dem Anrufer verfügbar. 
    
 _lppMessage_
  
> [out] Ein Zeiger auf einen Zeiger auf die neu erstellte Nachricht.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder::CreateMessage** -Methode erstellt eine neue Nachricht mit generischen oder zugehörigen Inhalte und weist einen Eintrag Bezeichner. Die Eintrags-ID besteht aus einer, die den Nachricht Speicheranbieter darstellt und einen Teil, der die einzelne Nachricht darstellt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können auswählen, ob alle erforderlichen Nachrichteneigenschaften in **CreateMessage** oder in der Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode festgelegt werden. Sie müssen keinen diese Eigenschaften zur Verfügung zu stellen, bis eine erfolgreiche speichern aufgetreten ist. 
  
Weitere Informationen zum Arbeiten mit zugehörigen Informationen finden Sie unter [Folder-Associated Informationen](folder-associated-information-tables.md) und [Inhalt Tabellen](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Einige Nachricht-Anbieter ermöglichen die Eintrags-ID der neuen Nachricht verfügbar sein soll, unmittelbar nachdem **CreateMessage** zurückgegeben. andere Anbieter Nachricht verzögert ihre Verfügbarkeit, bis die Nachricht gespeichert wird. Da nicht alle Anbieter Nachricht einen Eintrag Bezeichner für eine neue Nachricht generieren, bis Sie die Nachricht **IMAPIProp::SaveChanges** -Methode aufgerufen haben, können Sie möglicherweise nicht auf die Eintrags-ID zugreifen, wenn **CreateMessage** zurückgegeben. Darüber hinaus kann die neue Nachricht nicht in den Ordner Inhaltstabelle enthalten, bis der Speichervorgang. 
  
Erwarten Sie die Eintrags-ID zugewiesen, um die neue Nachricht nicht nur in der aktuellen Nachrichtenspeicher eindeutig, aber die sich am ehesten in allen der Nachrichtenspeicher sein, die gleichzeitig geöffnet sind. Eine Ausnahme zu dieser Regel tritt auf, wenn mehrere Einträge für einen Nachrichtenspeicher im Profil angezeigt werden. Daraufhin wird die Nachrichtenspeicher mehrmals geöffnet werden soll und Eintragsbezeichner dupliziert werden. 
  
Rufen Sie der Ordner Postausgang **IMAPIFolder::CreateMessage** -Methode, um eine ausgehende Nachricht zu erstellen. 
  
Wenn Sie einen Ordner löschen, der eine neue Nachricht enthält, bevor die Nachricht gespeichert wird, sind die Ergebnisse nicht definiert.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI (engl.) wird die **IMAPIFolder::CreateMessage** -Methode zum Erstellen und speichern Sie eine neue Nachricht verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

