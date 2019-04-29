---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426387"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Objekt und gibt einen Schnittstellenzeiger für zusätzlichen Zugriff zurück.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des zu öffnenden Objekts.
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll. Durch das Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Wenn das zu öffnende Objekt beispielsweise eine Nachricht ist, ist die Standardschnittstelle [IMessage](imessageimapiprop.md); für Ordner ist es [IMAPIFolder](imapifolderimapicontainer.md). Die Standardschnittstellen für Adressbuch Objekte sind [IDistList](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können verwendet werden:
    
MAPI_BEST_ACCESS 
  
> Fordert, dass das Objekt unter Verwendung der maximal für den Benutzer zulässigen Netzwerkberechtigungen und des maximalen Client Anwendungszugriffs geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte das Objekt mit Lese-/Schreibzugriff geöffnet werden. Wenn der Client schreibgeschützte Berechtigung hat, sollte das Objekt mit Leseberechtigung geöffnet werden. 
    
MAPI_CACHE_OK
  
> Verwenden Sie alle Mittel, einschließlich Offlineadressbüchern, um die Namensauflösung durchzuführen.
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** das erfolgreiche zurückgeben von OpenEntry, bevor das Objekt vollständig für den aufrufenden Client verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann das Ausführen eines nachfolgenden Objekt Aufrufs einen Fehler verursachen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte mit Schreibschutz Berechtigung geöffnet, und Clients sollten nicht mit der Annahme arbeiten, dass Lese-/Schreibzugriff erteilt wird. 
    
MAPI_NO_CACHE
  
> Verwenden Sie das Offlineadressbuch nicht zum Ausführen der Namensauflösung. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
SHOW_SOFT_DELETES
  
> Elemente anzeigen, die derzeit als "Soft Deleted" markiert sind (also in der Aufbewahrungszeit für gelöschte Elemente).
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> Out Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern, oder es wurde versucht, auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_FOUND 
  
> Es ist kein Objekt mit der im _lpEntryID_ -Parameter übergebenen Eintrags-ID verknüpft. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die im _lpEntryID_ -Parameter übergebene Eintrags-ID weist ein unbekanntes Format auf. Dieser Wert wird in der Regel zurückgegeben, wenn der Dienstanbieter, der das Objekt enthält, nicht geöffnet ist. 
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMAPISession:: OpenEntry** -Methode wird ein Nachrichtenspeicher-oder Adressbuchobjekt geöffnet, und es wird ein Zeiger auf eine Schnittstelle zurückgegeben, die für den Zugriff auf das Objekt verwendet werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

> [!IMPORTANT]
> Beim Öffnen von Ordnereinträgen in einem öffentlichen Informationsspeicher wie Ordner und Nachrichten verwenden Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) anstelle von **IMAPISession:: OpenEntry**. Dadurch wird sichergestellt, dass öffentliche Ordner ordnungsgemäß funktionieren, wenn mehrere Exchange-Konten in einem Profil definiert sind. 
  
Rufen Sie **IMAPISession:: OpenEntry** nur auf, wenn Sie nicht wissen, welche Art von Objekt Sie öffnen. Wenn Sie wissen, dass Sie einen Ordner oder eine Nachricht öffnen, rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md)auf. Wenn Sie wissen, dass Sie einen Adressbuchcontainer, einen Messagingbenutzer oder eine Verteilerliste öffnen, rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md)auf. Diese spezifischeren Methoden sind schneller als **IMAPISession:: OpenEntry**. 
  
MAPI öffnet alle Objekte mit Schreibschutz Berechtigung, es sei denn, Sie legen das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag im _ulFlags_ -Parameter fest. Das Festlegen eines dieser Flags garantiert keinen bestimmten Zugriffstyp. welche Berechtigungen erteilt werden, hängt vom Dienstanbieter, der Zugriffsebene und dem Objekt ab. Um die Zugriffsebene des geöffneten Objekts zu bestimmen, rufen Sie die **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft ab.
  
Das Aufrufen von **IMAPISession:: OpenEntry** und das Festlegen von _lpEntryID_ so, dass auf den Eintragsbezeichner eines Nachrichtenspeichers verwiesen wird, entspricht dem Aufrufen der [IMAPISession:: OPENMSGSTORE](imapisession-openmsgstore.md) -Methode mit dem MDB_NO_DIALOG-Flagsatz. Die Flageinstellungen sind ebenfalls äquivalent, mit der Ausnahme, dass zum Anfordern der Berechtigung zum Lesen/Schreiben mit **OpenMsgStore**das MDB_WRITE-Flag anstelle von MAPI_MODIFY festgelegt werden muss. 
  
Überprüfen Sie den Wert, der im _lpulObjType_ -Parameter zurückgegeben wird, um zu bestimmen, ob der zurückgegebene Objekttyp Ihren Erwartungen entspricht. Wenn der Objekttyp nicht der erwartete Typ ist, wandeln Sie den Zeiger vom _lppUnk_ -Parameter in einen Zeiger des entsprechenden Typs um. Wenn Sie beispielsweise einen Ordner öffnen, werfen Sie _lppUnk_ in einen Zeiger vom Typ LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI verwendet die **IMAPISession:: OpenEntry** -Methode, um ein Objekt zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

