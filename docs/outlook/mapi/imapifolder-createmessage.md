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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412632"
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
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf die neue Nachricht verwendet werden soll. Gültige Schnittstellenbezeichner sind IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder. Durch Übergeben von NULL gibt der Nachrichtenspeicheranbieter die Standardnachrichtenschnittstelle [IMessage : IMAPIProp zurück.](imessageimapiprop.md) 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachricht erstellt wird. Die folgenden Kennzeichen können festgelegt werden:
    
ITEMPROC_FORCE
  
> Gibt dem Persönlichen Ordnerspeicher (PST) an, dass die Nachricht für die Regelverarbeitung berechtigt ist, bevor der Speicher jeden Abhörclient über den Eintreffen der neuen Nachricht benachrichtigt. Die Verarbeitung von Regeln gilt nur für neue Nachrichten, die auf einem Server erstellt werden, der kein Microsoft Exchange Server ist, da Exchange Server Regeln für Nachrichten auf dem Server verarbeitet. Daher muss der Anbieter oder Client, der die Nachricht erstellt, dieses Flag in Kombination mit dem Speichern einer Nachricht mit [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) mithilfe von NON_EMS_XP_SAVE übergeben, was angibt, dass der Server kein Exchange Server. 
    
MAPI_ASSOCIATED 
  
> Die zu erstellende Nachricht sollte in der zugeordneten Inhaltstabelle anstelle der Standardinhaltstabelle enthalten sein. Zugeordnete Nachrichten werden aus der Benutzerinteraktion ausgeblendet.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** kann auch dann erfolgreich sein, wenn der Erstellungsvorgang noch nicht vollständig abgeschlossen ist. Dies bedeutet, dass die neue Nachricht möglicherweise nicht sofort für den Anrufer verfügbar ist. 
    
 _lppMessage_
  
> [out] Ein Zeiger auf einen Zeiger auf die neu erstellte Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::CreateMessage-Methode** erstellt eine neue Nachricht mit generischem oder zugeordneten Inhalt und weist einen Eintragsbezeichner zu. Der Eintragsbezeichner besteht aus einem Teil, der den Nachrichtenspeicheranbieter darstellt, und einem Teil, der die einzelne Nachricht darstellt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können auswählen, ob alle erforderlichen Nachrichteneigenschaften in **CreateMessage** oder in der [IMAPIProp::SaveChanges-Methode der](imapiprop-savechanges.md) Nachricht festgelegt werden. Sie müssen diese Eigenschaften erst verfügbar machen, wenn ein erfolgreiches Speichern erfolgt ist. 
  
Weitere Informationen zum Arbeiten mit zugeordneten Informationen finden Sie unter [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Einige Nachrichtenspeicheranbieter erlauben, dass der Eintragsbezeichner der neuen Nachricht unmittelbar nach der Rückgabe von **CreateMessage verfügbar** ist. Andere Nachrichtenspeicheranbieter verzögern die Verfügbarkeit, bis die Nachricht gespeichert wird. Da nicht alle Nachrichtenspeicheranbieter eine Eintrags-ID für eine neue Nachricht generieren, bis Sie die **IMAPIProp::SaveChanges-Methode** der Nachricht aufgerufen haben, können Sie möglicherweise nicht auf die Eintrags-ID zugreifen, wenn **CreateMessage** zurückgibt. Außerdem ist die neue Nachricht möglicherweise erst in der Inhaltstabelle des Ordners enthalten, wenn das Speichern erfolgt. 
  
Erwarten Sie, dass der der neuen Nachricht zugewiesene Eintragsbezeichner nicht nur im aktuellen Nachrichtenspeicher eindeutig ist, sondern höchstwahrscheinlich für alle gleichzeitig geöffneten Nachrichtenspeicher. Eine Ausnahme von dieser Regel tritt auf, wenn mehrere Einträge für einen Nachrichtenspeicher im Profil angezeigt werden. Dies bewirkt, dass der Nachrichtenspeicher mehrmals geöffnet wird, und Eintragsbezeichner werden dupliziert. 
  
Rufen Sie zum Erstellen einer ausgehenden Nachricht die **IMAPIFolder::CreateMessage-Methode des Postfachordners** auf. 
  
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

