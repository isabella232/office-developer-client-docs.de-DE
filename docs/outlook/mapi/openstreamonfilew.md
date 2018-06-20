---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 127c4a77b9184d8bb62925c5237c1aedec643992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793322"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

  
  
**Betrifft**: Outlook 
  
Reserviert und initialisiert ein OLE- **IStream** -Objekt Zugriff auf den Inhalt einer Datei. Diese Funktion akzeptiert Unicode-Zeichenfolgen als Argumente, im Gegensatz zu ANSI-Version dieser Funktion [OpenStreamOnFile nicht ausgeführt werden](openstreamonfile.md), und daher kann für beliebige Zeichen in den Dateinamen einschließlich der Erweiterungs Pfad und den Dateinamen.
  
|||
|:-----|:-----|
|Vom exportiert werden:  <br/> |olmapi32.dll  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameter

 _lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _ulFlags_
  
> [in] Bitmaske der Flags verwendet, um das Erstellen oder Öffnen der Datei steuern über das OLE- **IStream** -Objekt zugegriffen werden. Die folgenden Kennzeichen können festgelegt werden: 
    
SOF_UNIQUEFILENAME
  
> Eine temporäre Datei ist für das **IStream** -Objekt erstellt werden soll. Wenn dieses Flag festgelegt ist, sollte die Flags STGM_CREATE und Accessor auch festgelegt werden. 
    
STGM_CREATE
  
> Die Datei ist erstellt werden soll, auch wenn Sie bereits vorhanden. Wenn der Parameter _LpszFileName_ nicht festgelegt ist, muss dieses Flag und die STGM_DELETEONRELEASE festgelegt werden. Wenn STGM_CREATE festgelegt ist, muss auch die Accessor-Flag festgelegt werden. 
    
STGM_DELETEONRELEASE
  
> Die Datei wird gelöscht, wenn das Objekt **IStream** freigegeben wird. Wenn der Parameter _LpszFileName_ nicht festgelegt ist, muss dieses Flag und die STGM_CREATE festgelegt werden. 
    
BEISPIELCODEZEILEN
  
> Die Datei wird mit schreibgeschützten Zugriff geöffnet oder erstellt werden.
    
ACCESSOR
  
> Die Datei wird erstellt oder mit Lese-/Schreibzugriff geöffnet werden soll. Wenn dieses Flag nicht festgelegt ist, muss das Flag STGM_CREATE nicht festgelegt werden.
    
 _lpszFileName_
  
> [in] Der Dateiname mit dem Namen einschließlich Pfad und Erweiterung des Unicode-Datei für die **OpenStreamOnFileW** **IStream** -Objekt initialisiert. Wenn das Flag SOF_UNIQUEFILENAME festgelegt ist, enthält _LpszFileName_ den Pfad zu dem Verzeichnis, in dem Sie eine temporäre Datei zu erstellen. Wenn _LpszFileName_ NULL ist, **OpenStreamOnFileW** ruft geeigneten Pfad aus dem System und die STGM_CREATE und die STGM_DELETEONRELEASE Flags müssen festgelegt werden. 
    
 _lpszPrefix_
  
> [in] Das Präfix für den Unicode-Dateinamen auf dem **OpenStreamOnFileW** **IStream** -Objekt initialisiert. Wenn festgelegt, das Präfix nicht mehr als drei Zeichen enthalten muss. Wenn _LpszPrefix_ NULL ist, wird das Präfix "SOF" verwendet. 
    
 _lppStream_
  
> [out] Zeiger auf einen Zeiger auf ein Objekt, das die **IStream** -Schnittstelle verfügbar macht. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_ACCESS
  
> Die Datei konnte nicht zugegriffen werden, aufgrund der nicht über ausreichende Benutzerberechtigungen oder da schreibgeschützte Dateien nicht geändert werden können.
    
MAPI_E_NOT_FOUND
  
> Die angegebene Datei ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **OpenStreamOnFileW** -Funktion besitzt zwei wichtige Verwendungen neben der Behandlung von einer Datei mit einem Unicode-Namen, durch die Einstellung des Flags SOF_UNIQUEFILENAME unterschieden. Wenn dieses Flag nicht festgelegt ist, wird **OpenStreamOnFileW** **IStream** -Objekts auf eine vorhandene Datei, zum Beispiel zum Kopieren von seinen Inhalt der **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))-Eigenschaft einer Anlage, die mit der **geöffnet. :: CopyTo** Methode. In diesem Fall gibt der Parameter _LpszFileName_ den Pfad und Dateinamen der Datei an. 
  
Wenn SOF_UNIQUEFILENAME festgelegt ist, erstellt **OpenStreamOnFileW** eine temporäre Datei zum Speichern von Daten für **IStream** -Objekts. Für diese Verwendung kann der Parameter _LpszFileName_ optional bestimmen den Pfad zu dem Verzeichnis, in dem die Datei erstellt werden soll, und der Parameter _LpszPrefix_ kann optional ein Präfix für den Dateinamen angeben. 
  
Wenn mit dem **IStream** -Objekt den aufrufenden Clientanwendung oder den Dienstanbieter abgeschlossen ist, sollten sie es durch Aufrufen der Methode OLE **Streamkomponente IStream::** frei. 
  
MAPI verwendet die Funktionen, auf die _LpAllocateBuffer_ und _LpFreeBuffer_ für die meisten Zuweisung von virtuellem Speicher und zur Freigabe, insbesondere, um für die Verwendung von Clientanwendungen Speicher beim Aufruf von Schnittstellen für Objekte wie [IMAPIProp:: GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Das Flag SOF_UNIQUEFILENAME wird verwendet, um eine temporäre Datei durch einen Namen für die messaging-System eindeutig zu erstellen. Wenn dieses Flag festgelegt ist, enthält die _LpszFileName_ -Parameter gibt den Pfad für die temporäre Datei und der _LpszPrefix_ -Parameter die Anfangszeichen des Dateinamens. Der erstellte Dateiname ist <prefix>HHHH. TMP, wobei HHHH eine hexadezimale Zahl ist. Wenn _LpszFileName_ NULL ist, wird die Datei im Verzeichnis temporäre Datei, das von der Windows-Funktion **GetTempPath**zurückgegeben wird, oder das aktuelle Verzeichnis erstellt, wenn kein Verzeichnis temporäre Datei vorgesehen ist.
  
Wenn das Flag SOF_UNIQUEFILENAME nicht festgelegt ist, _LpszPrefix_ wird ignoriert, und der vollständig qualifizierte Pfad und Dateiname der Datei geöffnet oder erstellt werden, sollte _LpszFileName_ enthalten. Die Datei wird geöffnet oder erstellt basierend auf den anderen Flags, die in _UlFlags_festgelegt sind.
  
## <a name="see-also"></a>Siehe auch



[OpenStreamOnFile nicht ausgeführt werden](openstreamonfile.md)

