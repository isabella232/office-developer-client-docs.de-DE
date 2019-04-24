---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348629"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Reserviert und initialisiert ein OLE **IStream** -Objekt, um auf den Inhalt einer Datei zuzugreifen. Diese Funktion verwendet eine ANSI-Zeichenfolge als Dateinamen, einschließlich des Pfads und der Dateierweiterung, daher wird die Verwendung der Unicode-Version dieser Funktion, [OpenStreamOnFileW](openstreamonfilew.md), empfohlen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _ulFlags_
  
> in Bitmaske der Flags, die zum Steuern des Erstellens oder Öffnens der Datei verwendet werden, auf die über das **IStream** -Objekt von OLE zugegriffen werden kann. Die folgenden Flags können festgelegt werden: 
    
SOF_UNIQUEFILENAME 
  
> Für das **IStream** -Objekt muss eine temporäre Datei erstellt werden. Wenn dieses Flag festgelegt ist, sollten auch die STGM_CREATE-und STGM_READWRITE-Flags festgelegt werden. 
    
STGM_CREATE 
  
> Die Datei muss auch dann erstellt werden, wenn Sie bereits vorhanden ist. Wenn der _lpszFileName_ -Parameter nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_DELETEONRELEASE festgelegt werden. Wenn STGM_CREATE festgelegt ist, muss auch das STGM_READWRITE-Flag festgelegt werden. 
    
STGM_DELETEONRELEASE 
  
> Die Datei muss gelöscht werden, wenn das **IStream** -Objekt freigegeben wird. Wenn der _lpszFileName_ -Parameter nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_CREATE festgelegt werden. 
    
STGM_READ 
  
> Die Datei muss mit Schreibschutz erstellt oder geöffnet werden. 
    
STGM_READWRITE 
  
> Die Datei muss mit Lese-/Schreibzugriff erstellt oder geöffnet werden. Wenn dieses Flag nicht festgelegt ist, darf das STGM_CREATE-Flag nicht festgelegt werden. 
    
 _lpszFileName_
  
> in Der Dateiname, einschließlich Pfad und Erweiterung der Datei, für die **OpenStreamOnFile** das **IStream** -Objekt initialisiert. Wenn das SOF_UNIQUEFILENAME-Flag festgelegt ist, enthält _lpszFileName_ den Pfad zu dem Verzeichnis, in dem eine temporäre Datei erstellt werden soll. Wenn _lpszFileName_ ist, ruft **OpenStreamOnFile** einen entsprechenden Pfad vom System ab, und sowohl die STGM_CREATE-als auch die STGM_DELETEONRELEASE-Flags müssen festgelegt werden. 
    
 _lpszPrefix_
  
> in Das Präfix für den Dateinamen, auf dem **OpenStreamOnFile** das **IStream** -Objekt initialisiert. Wenn diese Einstellung festgelegt ist, darf das Präfix nicht mehr als drei Zeichen enthalten. Wenn _lpszPrefix_ ist, wird ein Präfix von "Sof" verwendet. 
    
 _lppStream_
  
> Out Zeiger auf einen Zeiger auf ein Objekt, das die **IStream** -Schnittstelle verfügbar macht. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_NO_ACCESS 
  
> Auf die Datei konnte aufgrund unzureichender Benutzerberechtigungen nicht zugegriffen werden, oder da schreibgeschützte Dateien nicht geändert werden können. 
    
MAPI_E_NOT_FOUND 
  
> Die angegebene Datei ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **OpenStreamOnFile** -Funktion verfügt über zwei wichtige Verwendungsweisen, die durch die Einstellung des SOF_UNIQUEFILENAME-Flags unterschieden werden. Wenn dieses Flag nicht festgelegt ist, wird von **OpenStreamOnFile** ein **IStream** -Objekt für eine vorhandene Datei geöffnet, beispielsweise zum Kopieren des Inhalts in die **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md))-Eigenschaft einer Anlage mithilfe von **IStream. :: CopyTo** -Methode. In diesem Fall gibt der Parameter _lpszFileName_ den Pfad und den Dateinamen der Datei an. 
  
Wenn SOF_UNIQUEFILENAME festgelegt ist, erstellt **OpenStreamOnFile** eine temporäre Datei zum Speichern von Daten für ein **IStream** -Objekt. Für diese Verwendung kann der Parameter _lpszFileName_ optional den Pfad zu dem Verzeichnis festlegen, in dem die Datei erstellt werden soll, und der Parameter _lpszPrefix_ kann optional ein Präfix für den Dateinamen angeben. 
  
Wenn die aufrufende Clientanwendung oder der Dienstanbieter mit dem **IStream** -Objekt fertig ist, sollten Sie diese freigeben, indem Sie die OLE **IStream:: Release** -Methode aufrufen. 
  
MAPI verwendet die Funktionen, auf die von _lpAllocateBuffer_ und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen, insbesondere für die Zuweisung von Arbeitsspeicher für Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp:: ](imapiprop-getprops.md)GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Das SOF_UNIQUEFILENAME-Flag wird verwendet, um eine temporäre Datei mit einem eindeutigen Namen für das Messagingsystem zu erstellen. Wenn dieses Flag festgelegt ist, angibt der _lpszFileName_ -Parameter den Pfad für die temporäre Datei, und der _lpszPrefix_ -Parameter enthält die Präfixzeichen des Datei namens. Der erstellte Dateiname lautet <prefix>HHHH. TMP, wobei HHHH eine Hexadezimalzahl ist. Wenn _lpszFileName_ ist, wird die Datei im temporären Dateiverzeichnis erstellt, das von der Windows-Funktion **GetTempPath**zurückgegeben wird, oder das aktuelle Verzeichnis, wenn kein temporäres Dateiverzeichnis festgelegt wurde. 
  
Wenn das SOF_UNIQUEFILENAME-Flag nicht festgelegt ist, wird _lpszPrefix_ ignoriert, und _lpszFileName_ sollte den vollqualifizierten Pfad und Dateinamen der zu öffnenden oder zu erstellenden Datei enthalten. Die Datei wird basierend auf den anderen in _ulFlags_festgelegten Flags geöffnet oder erstellt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Datei. cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI verwendet die **OpenStreamOnFile** -Methode, um einen Stream für eine Datei zu öffnen, damit eine Anlage an Sie ausgeschrieben werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

