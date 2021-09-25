---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 426ca9a33444f6130f8ee4eca62164bc835a032c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551415"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine neue Nachricht.
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf die neue Nachricht verwendet werden soll. Gültige Schnittstellenbezeichner sind IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder. Wenn NULL übergeben wird, gibt der Nachrichtenspeicheranbieter die Standardmäßige Nachrichtenschnittstelle [IMessage : IMAPIProp](imessageimapiprop.md)zurück. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachricht erstellt wird. Die folgenden Flags können festgelegt werden:
    
ITEMPROC_FORCE
  
> Gibt dem persönlichen Ordnerspeicher (PERSONAL FOLDER STORE, PST) an, dass die Nachricht für die Verarbeitung von Regeln berechtigt ist, bevor der Speicher einen Überwachungsclient über die Einführung der neuen Nachricht benachrichtigt. Die Regelverarbeitung gilt nur für neue Nachrichten, die auf einem Server erstellt werden, der kein Microsoft Exchange Server ist, da Exchange Server Regeln für Nachrichten auf dem Server verarbeitet. Daher muss der Anbieter oder Client, der die Nachricht erstellt, dieses Flag in Kombination mit dem Speichern einer Nachricht mit [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) mit NON_EMS_XP_SAVE übergeben, was bedeutet, dass der Server kein Exchange Server ist. 
    
MAPI_ASSOCIATED 
  
> Die zu erstellende Nachricht sollte nicht im Standardinhaltsverzeichnis, sondern im zugeordneten Inhaltsverzeichnis enthalten sein. Zugeordnete Nachrichten werden vor Benutzerinteraktionen ausgeblendet.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** kann auch dann erfolgreich ausgeführt werden, wenn der Erstellungsvorgang nicht vollständig abgeschlossen wurde. Dies bedeutet, dass die neue Nachricht möglicherweise nicht sofort für den Aufrufer verfügbar ist. 
    
 _lppMessage_
  
> [out] Ein Zeiger auf einen Zeiger auf die neu erstellte Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich erstellt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::CreateMessage-Methode** erstellt eine neue Nachricht mit generischem oder zugeordneten Inhalt und weist einen Eintragsbezeichner zu. Der Eintragsbezeichner besteht aus einem Teil, der den Nachrichtenspeicheranbieter darstellt, und einem Teil, der die einzelne Nachricht darstellt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können auswählen, ob alle erforderlichen Nachrichteneigenschaften in **CreateMessage** oder in der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht festgelegt werden sollen. Sie müssen diese Eigenschaften erst verfügbar machen, wenn ein erfolgreiches Speichern erfolgt ist. 
  
Weitere Informationen zum Arbeiten mit zugeordneten Informationen finden Sie unter [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Einige Nachrichtenspeicheranbieter lassen zu, dass der Eintragsbezeichner der neuen Nachricht unmittelbar nach der Rückgabe von **CreateMessage** verfügbar ist. Andere Nachrichtenspeicheranbieter verzögern die Verfügbarkeit, bis die Nachricht gespeichert wird. Da nicht alle Nachrichtenspeicheranbieter einen Eintragsbezeichner für eine neue Nachricht generieren, bis Sie die **IMAPIProp::SaveChanges-Methode** der Nachricht aufgerufen haben, können Sie möglicherweise nicht auf den Eintragsbezeichner zugreifen, wenn **CreateMessage** zurückgegeben wird. Außerdem kann die neue Nachricht erst dann in das Inhaltsverzeichnis des Ordners aufgenommen werden, wenn das Speichern erfolgt. 
  
Erwarten Sie, dass der Eintragsbezeichner, der der neuen Nachricht zugewiesen ist, nicht nur im aktuellen Nachrichtenspeicher eindeutig ist, sondern höchstwahrscheinlich in allen Nachrichtenspeichern, die gleichzeitig geöffnet sind. Eine Ausnahme von dieser Regel tritt auf, wenn mehrere Einträge für einen Nachrichtenspeicher im Profil angezeigt werden. Dadurch wird der Nachrichtenspeicher mehrmals geöffnet, und Eintragsbezeichner werden dupliziert. 
  
Rufen Sie zum Erstellen einer ausgehenden Nachricht die **IMAPIFolder::CreateMessage-Methode** des Ordners "Postausgang" auf. 
  
Wenn Sie einen Ordner löschen, der eine neue Nachricht enthält, bevor die Nachricht gespeichert wird, sind die Ergebnisse nicht definiert.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI verwendet die **IMAPIFolder::CreateMessage-Methode,** um eine neue Nachricht zu erstellen und zu speichern.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

