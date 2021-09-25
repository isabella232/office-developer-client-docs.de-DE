---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f75f781c00fc4fe202e14bc955b2099ffb9ccdbc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575337"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Weist ein OLE **IStream-Objekt** zu und initialisiert es, um auf den Inhalt einer Datei zuzugreifen. Diese Funktion verwendet eine ANSI-Zeichenfolge als Dateinamen einschließlich Pfad und Dateierweiterung. Daher wird die Verwendung der Unicode-Version dieser Funktion, [OpenStreamOnFileW,](openstreamonfilew.md)empfohlen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameter

 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freigeben von Arbeitsspeicher verwendet werden soll. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die zum Steuern der Erstellung oder des Öffnens der Datei verwendet werden, auf die über das OLE **IStream-Objekt** zugegriffen werden soll. Die folgenden Flags können festgelegt werden: 
    
SOF_UNIQUEFILENAME 
  
> Für das **IStream-Objekt** soll eine temporäre Datei erstellt werden. Wenn dieses Flag festgelegt ist, sollten auch die Flags STGM_CREATE und STGM_READWRITE festgelegt werden. 
    
STGM_CREATE 
  
> Die Datei soll auch dann erstellt werden, wenn bereits eine vorhanden ist. Wenn der  _Parameter lpszFileName_ nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_DELETEONRELEASE festgelegt werden. Wenn STGM_CREATE festgelegt ist, muss auch das STGM_READWRITE-Flag festgelegt werden. 
    
STGM_DELETEONRELEASE 
  
> Die Datei soll gelöscht werden, wenn das **IStream-Objekt** freigegeben wird. Wenn der  _Parameter lpszFileName_ nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_CREATE festgelegt werden. 
    
STGM_READ 
  
> Die Datei soll mit schreibgeschütztem Zugriff erstellt oder geöffnet werden. 
    
STGM_READWRITE 
  
> Die Datei soll mit Lese-/Schreibberechtigung erstellt oder geöffnet werden. Wenn dieses Kennzeichen nicht festgelegt ist, darf auch das STGM_CREATE Flag nicht festgelegt werden. 
    
 _lpszFileName_
  
> [in] Der Dateiname einschließlich Pfad und Erweiterung der Datei, für die **OpenStreamOnFile** das **IStream-Objekt** initialisiert. Wenn das flag SOF_UNIQUEFILENAME festgelegt ist, enthält  _lpszFileName_ den Pfad zum Verzeichnis, in dem eine temporäre Datei erstellt werden soll. Wenn  _lpszFileName_ NULL ist, ruft **OpenStreamOnFile** einen geeigneten Pfad vom System ab, und die Flags STGM_CREATE und STGM_DELETEONRELEASE müssen festgelegt werden. 
    
 _lpszPrefix_
  
> [in] Das Präfix für den Dateinamen, mit dem **OpenStreamOnFile** das **IStream-Objekt** initialisiert. Wenn festgelegt, darf das Präfix nicht mehr als drei Zeichen enthalten. Wenn  _lpszPrefix_ NULL ist, wird das Präfix "SOF" verwendet. 
    
 _lppStream_
  
> [out] Zeiger auf einen Zeiger auf ein Objekt, das die **IStream-Schnittstelle** verfügbar machen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_NO_ACCESS 
  
> Auf die Datei konnte aufgrund unzureichender Benutzerberechtigungen oder aufgrund von schreibgeschützten Dateien nicht zugegriffen werden. 
    
MAPI_E_NOT_FOUND 
  
> Die angegebene Datei ist nicht vorhanden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **OpenStreamOnFile-Funktion** hat zwei wichtige Verwendungsmöglichkeiten, die sich durch die Einstellung des SOF_UNIQUEFILENAME Flags unterscheiden. Wenn dieses Kennzeichen nicht festgelegt ist, öffnet **OpenStreamOnFile** ein **IStream-Objekt** in einer vorhandenen Datei, z. B. um den Inhalt in die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) -Eigenschaft einer Anlage mithilfe der **IStream::CopyTo** -Methode zu kopieren. In diesem Fall gibt der  _Parameter lpszFileName_ den Pfad und den Dateinamen der Datei an. 
  
Wenn SOF_UNIQUEFILENAME festgelegt ist, erstellt **OpenStreamOnFile** eine temporäre Datei, die Daten für ein **IStream-Objekt** enthält. Für diese Verwendung kann der Parameter  _lpszFileName_ optional den Pfad zum Verzeichnis angeben, in dem die Datei erstellt werden soll, und der  _Parameter lpszPrefix_ kann optional ein Präfix für den Dateinamen angeben. 
  
Wenn die aufrufende Clientanwendung oder der aufrufende Dienstanbieter mit dem **IStream-Objekt** fertig ist, sollte es durch Aufrufen der OLE **IStream::Release-Methode** freigegeben werden. 
  
DIE MAPI verwendet die Funktionen, auf die _lpAllocateBuffer_ und _lpFreeBuffer_ verweisen, für die meisten Speicherzuweisungen und Freigaben, insbesondere zum Zuordnen von Arbeitsspeicher zur Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows.](imapitable-queryrows.md) 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Das flag SOF_UNIQUEFILENAME wird verwendet, um eine temporäre Datei mit einem eindeutigen Namen für das Messagingsystem zu erstellen. Wenn dieses Flag festgelegt ist, gibt der Parameter  _lpszFileName_ den Pfad für die temporäre Datei an, und der  _Parameter lpszPrefix_ enthält die Präfixzeichen des Dateinamens. Der erstellte Dateiname ist <prefix> HHHH. TMP, wobei HHHH eine Hexadezimalzahl ist. Wenn _lpszFileName_ NULL ist, wird die Datei im temporären Dateiverzeichnis erstellt, das von der Windows-Funktion **GetTempPath** zurückgegeben wird, oder im aktuellen Verzeichnis, wenn kein temporäres Dateiverzeichnis festgelegt wurde. 
  
Wenn das SOF_UNIQUEFILENAME Flag nicht festgelegt ist, wird  _lpszPrefix_ ignoriert, und  _lpszFileName_ sollte den vollqualifizierten Pfad und Dateinamen der zu öffnenden oder zu erstellenden Datei enthalten. Die Datei wird geöffnet oder basierend auf den anderen Flags erstellt, die in  _ulFlags_ festgelegt sind. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI verwendet die **OpenStreamOnFile-Methode,** um einen Datenstrom in einer Datei zu öffnen, damit eine Anlage in die Datei geschrieben werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

