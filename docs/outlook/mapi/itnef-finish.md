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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435677"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beendet die Verarbeitung für alle Transport-Neutral Encapsulation Format (TNEF), die in die Warteschlange eingereiht und gewartet werden. 
  
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
  
> [out] Ein Zeiger auf **die PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Schlüsseleigenschaft einer Anlage. Das TNEF-Kapselungsobjekt verwendet diesen Schlüssel, um eine Anlage mit dem Anlagenplatzierungstag in einer Nachricht zu versehen. Dieser Schlüssel sollte für jede Anlage eindeutig sein.
    
 _lpProblem_
  
> [out] Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray-Struktur.](stnefproblemarray.md) Die **STnefProblemArray-Struktur** gibt an, welche Eigenschaften, falls welche, nicht ordnungsgemäß codiert wurden. Wenn NULL im  _lpProblem-Parameter_ übergeben wird, wird kein Array mit Eigenschaftsproblemen zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::Finish-Methode** auf, um die Codierung aller Eigenschaften durchzuführen, für die die Codierung in Aufrufen der [Methoden ITnef::AddProps](itnef-addprops.md) und [ITnef::SetProps angefordert](itnef-setprops.md) wurde. Wenn das TNEF-Objekt mit dem flag TNEF_ENCODE für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion](opentnefstreamex.md) geöffnet wurde, codiert die **Finish-Methode** die angeforderten Eigenschaften in den an dieses Objekt übergebenen Kapselungsstream. Wenn das TNEF-Objekt mit dem flag TNEF_DECODE geöffnet wurde, decodiert die **Finish-Methode** die Eigenschaften aus dem TNEF-Stream und schreibt sie zurück in die Nachricht, zu der sie gehören. 
  
Nach dem **Aufruf Fertig** stellen zeigt der Zeiger auf den Kapselungsstream auf das Ende der TNEF-Daten. Wenn der Anbieter oder das Gateway die Daten des TNEF-Datenstroms nach dem **Aufruf** Beenden verwenden muss, muss der Datenstromzeiger auf den Anfang der TNEF-Daten zurückgesetzt werden. 
  
Die TNEF-Implementierung meldet TNEF-Streamcodierungsprobleme, ohne den **Fertig stellen-Prozess zu** beenden. Die im _lpProblem-Parameter_ zurückgegebene [STnefProblemArray-Struktur](stnefproblemarray.md) gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften (falls welche) nicht verarbeitet werden konnten. Der im **scode-Element** der in **STnefProblemArray enthaltene STnefProblemProblem-Struktur** zurückgegebene Wert gibt das spezifische Problem an.  Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **Finish** keinen Problembericht zurück gibt, erfolgreich verarbeitet wurden. 
  
Wenn ein Anbieter oder Gateway nicht mit Problemarrays funktioniert, kann er NULL in  _lpProblem übergeben._ In diesem Fall wird kein Problemarray zurückgegeben. 
  
Der in  _lpProblem_ zurückgegebene Wert ist nur gültig, wenn der Aufruf S_OK. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der **STnefProblemArray-Struktur** zurückgegebenen Werte überprüfen. Wenn beim Anruf ein Fehler auftritt, wird die **STnefProblemArray-Struktur** nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder frei geben. Wenn beim Anruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Arbeitsspeicher für **das STnefProblemArray** durch Aufrufen der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) frei geben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI verwendet die **ITnef::Finish-Methode,** um die Verarbeitung des neuen TNEF-Datenstroms zu beenden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber (kanonische Eigenschaft)](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

