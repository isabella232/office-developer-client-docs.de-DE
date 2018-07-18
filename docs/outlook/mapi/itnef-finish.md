---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2b95e0dd62d83dd83a064ee4627811fcb24af921
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792867"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Betrifft**: Outlook 
  
Beendet Verarbeitung für alle Transport-Neutral Encapsulation Format (TNEF) Vorgänge, die sich in der Warteschlange und wartet. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpKey_
  
> [out] Ein Zeiger auf die wichtigste **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage. Das TNEF-Kapselung-Objekt verwendet diesen Schlüssel mit dem entsprechenden Anlage Platzierung Tag in einer Nachricht eine Anlage übereinstimmt. Dieser Schlüssel sollte für jede Anlage eindeutig sein.
    
 _lpProblem_
  
> [out] Ein Zeiger auf einen Zeiger auf eine zurückgegebenen [STnefProblemArray](stnefproblemarray.md) -Struktur. Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden. Wenn NULL in der _LpProblem_ -Parameter übergeben wird, wird kein Problem Array-Eigenschaft zurückgegeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Transport-Provider, Anbieter Nachricht und Gateways Aufruf die **ITnef::Finish** -Methode zum Ausführen der Codierung aller Eigenschaften für die Codierung Aufrufe der Methoden [ITnef::AddProps](itnef-addprops.md) und [ITnef::SetProps](itnef-setprops.md) angefordert wurde. Wenn das TNEF-Objekt mit dem TNEF_ENCODE-Flag für die [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet wurde, codiert die Methode **Fertig stellen** die angeforderten Eigenschaften in der an dieses Objekt übergebene Encapsulation Stream. Wenn das TNEF-Objekt mit dem TNEF_DECODE-Flag geöffnet wurde, wird die Methode **Fertig stellen** decodiert die Eigenschaften aus dem TNEF-Stream und schreibt sie zurück in die Nachricht, der sie angehören. 
  
Nach dem Aufruf von **Fertig stellen** der Zeiger in den Stream Kapselung bis zum Ende der TNEF Daten zeigt. Wenn der Anbieter oder Gateway muss die TNEF-Stream-Daten verwenden Sie nach dem Aufrufen der **Fertig stellen** , muss es den Zeiger Stream an den Anfang der Streamdaten TNEF zurücksetzen. 
  
Die TNEF-Implementierung meldet TNEF Stream Codierung Probleme ohne Anhalten des Prozesses **Fertig stellen** . Die [STnefProblemArray](stnefproblemarray.md) -Struktur zurückgegeben, die in der _LpProblem_ -Parameter gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnte. Der im **Scode** -Member, eine der in **STnefProblemArray** enthaltenen **STnefProblem** Strukturen zurückgegebene Wert gibt an, das Problem. Der Anbieter oder Gateway kann auf der Annahme arbeiten, dass alle Eigenschaften oder Attribute für die **Fertig stellen** kein Problemberichts zurückgibt erfolgreich verarbeitet wurden. 
  
Wenn Sie einen Anbieter oder ein Gateway mit Problem Arrays nicht funktionsfähig ist, können sie NULL _LpProblem_übergeben; In diesem Fall wird kein Problem Array zurückgegeben. 
  
Der in _LpProblem_ zurückgegebene Wert ist nur gültig, wenn der Aufruf gibt S_OK zurück. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder ein Gateway in der Struktur **STnefProblemArray** zurückgegebenen Werte überprüfen. Bei einem beim Aufruf Fehler die **STnefProblemArray** -Struktur ist nicht ausgefüllt und die aufrufende Anbieter oder das Gateway nicht verwenden oder die Struktur frei. Wenn dem Gespräch tritt kein Fehler auf, muss die aufrufende Anbieter oder Gateway den Speicher freizugeben für die **STnefProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI (engl.) verwendet die **ITnef::Finish** -Methode des neuen TNEF-Streams abgeschlossen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber (kanonische Eigenschaft)](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

