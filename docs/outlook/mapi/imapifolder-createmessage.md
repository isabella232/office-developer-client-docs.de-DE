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
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280085"
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
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf die neue Nachricht verwendet werden soll. Gültige Schnittstellenbezeichner sind IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder. Durch das Übergeben von NULL wird der Nachrichtenspeicher Anbieter zur Standardnachrichten Schnittstelle, [IMessage: IMAPIProp](imessageimapiprop.md), zurückgegeben. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Erstellung der Nachricht steuert. Die folgenden Flags können festgelegt werden:
    
ITEMPROC_FORCE
  
> Gibt dem persönlichen Ordnerspeicher (PST) an, dass die Nachricht für die Verarbeitung von Regeln berechtigt ist, bevor der Informationsspeicher einen überwachenden Client über das Eintreffen der neuen Nachricht benachrichtigt. Die Regelverarbeitung gilt nur für neue Nachrichten, die auf einem Server erstellt werden, der kein Microsoft Exchange Server ist, da Exchange Server Regeln für Nachrichten auf dem Server verarbeitet. Daher muss der Anbieter oder Client, der die Nachricht erstellt, dieses Flag in Kombination mit dem Speichern einer Nachricht mit [IMAPIPProp:: SaveChanges](imapiprop-savechanges.md) mit NON_EMS_XP_SAVE, die angibt, dass es sich bei dem Server nicht um einen Exchange-Server handelt. 
    
MAPI_ASSOCIATED 
  
> Die zu erstellende Nachricht sollte in der Tabelle mit den verknüpften Inhalten und nicht in der Tabelle mit den Standardinhalten enthalten sein. Zugeordnete Nachrichten werden vor der Benutzerinteraktion ausgeblendet.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** kann auch dann erfolgreich ausgeführt werden, wenn der Erstellungsvorgang nicht vollständig abgeschlossen wurde. Dies impliziert, dass die neue Nachricht möglicherweise nicht sofort für den Anrufer verfügbar ist. 
    
 _lppMessage_
  
> Out Ein Zeiger auf einen Zeiger auf die neu erstellte Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder:: CreateMessage** -Methode erstellt eine neue Nachricht mit generischem oder zugehörigem Inhalt und weist eine Eintrags-ID zu. Die Eintrags-ID besteht aus einem Teil, der den Nachrichtenspeicher Anbieter darstellt, und einem Teil, der die einzelne Nachricht darstellt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können auswählen, ob alle erforderlichen Nachrichteneigenschaften in CreateMessage oder **** in der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht festgelegt werden sollen. Sie müssen diese Eigenschaften erst verfügbar machen, wenn ein erfolgreicher Speichervorgang stattgefunden hat. 
  
Weitere Informationen zum Arbeiten mit zugeordneten Informationen finden Sie unter [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Einige Nachrichtenspeicher Anbieter ermöglichen, dass die Eintrags-ID der neuen Nachricht sofort verfügbar **** ist, nachdem CreateMessage zurückgegeben wird. andere Nachrichtenspeicher Anbieter verzögern die Verfügbarkeit, bis die Nachricht gespeichert wird. Da nicht alle Nachrichtenspeicher Anbieter eine Eintrags-ID für eine neue Nachricht generieren, wenn Sie die **IMAPIProp:: SaveChanges** -Methode der Nachricht aufgerufen haben, können Sie möglicherweise nicht auf die Eintrags-ID zugreifen, wenn CreateMessage zurückgegeben wird. **** Außerdem wird die neue Nachricht möglicherweise erst in die Inhaltstabelle des Ordners aufgenommen, wenn die Speicherung erfolgt ist. 
  
Es wird davon ausgegangen, dass die der neuen Nachricht zugewiesene Eintrags-ID nicht nur im aktuellen Nachrichtenspeicher, sondern wahrscheinlich auch in allen Nachrichten speichern, die gleichzeitig geöffnet sind, eindeutig ist. Eine Ausnahme zu dieser Regel tritt auf, wenn mehrere Einträge für einen Nachrichtenspeicher im Profil angezeigt werden. Dies bewirkt, dass der Nachrichtenspeicher mehrmals geöffnet und Eintrags-IDs dupliziert werden. 
  
Um eine ausgehende Nachricht zu erstellen, rufen Sie die **IMAPIFolder:: CreateMessage** -Methode des Postausgangs Ordners auf. 
  
Wenn Sie einen Ordner mit einer neuen Nachricht löschen, bevor die Nachricht gespeichert wird, sind die Ergebnisse nicht definiert.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolder:: OnNewMessage  <br/> |MFCMAPI verwendet die **IMAPIFolder:: CreateMessage** -Methode, um eine neue Nachricht zu erstellen und zu speichern.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

