---
title: Fehlerbehandlung in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6f0ebd2112b65140a106a1376896f6de9c00da1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791636"
---
# <a name="error-handling-in-mapi"></a>Fehlerbehandlung in MAPI

**Betrifft**: Outlook 
  
Erfolg, Warnung und Fehler-Werte werden unter Verwendung einer 32-Bit-Version bekannte dementsprechend Handle oder HRESULT zurückgegeben. Ein HRESULT ist nicht wirklich ein Handle auf einen anderen Wert. Es wird lediglich eine 32-Bit-Wert mit mehrere Felder in den Wert codiert. Ein NULL-Ergebnis zeigt Erfolg und ein ungleich NULL Ergebnis Fehler.
  
MAPI auf 32-Bit-Plattformen funktioniert nur mit HRESULT-Werte.
  
Die folgende Abbildung zeigt das HRESULT-Format für 32-Bit-Plattformen.
  
**HRESULT-Format**
  
![HRESULT-format] (media/amapi_49.gif "HRESULT-format")
  
Das hohe Bit in der HRESULT gibt an, ob der Rückgabewert Erfolg oder Fehler darstellt. Wenn der Wert Erfolg gibt 0 (null) festgelegt, an. Wenn auf 1 festgelegt, es einen Fehler angibt.
  
Die R, C, N und R Bits sind in der HRESULT reserviert.
  
Das Feld Facility in beiden Versionen gibt den Bereich der Verantwortung für den Fehler. Es gibt verschiedene Funktionen, aber die Mehrheit der MAPI-Fehler verwenden FACILITY_ITF Benutzeroberflächenfehler darstellen. Werden die am häufigsten verwendeten Funktionen, die derzeit verwendet werden: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC und FACILITY_STORAGE. Wenn neue Funktionen erforderlich sind, weist Microsoft sie, da sie eindeutig sein müssen. In der folgenden Tabelle werden die verschiedenen Facility Felder beschrieben.
  
|Einrichtung|Beschreibung|
|:-----|:-----|
|FACILITY_NULL  <br/> |Für umfassend anwendbaren allgemeine Statuscodes wie S_OK oder E_OUTOF_MEMORY; der Wert ist NULL.  <br/> |
|FACILITY_ITF  <br/> |Für die meisten Statuscodes von Schnittstellenmethoden zurückgegeben; der Wert wird von der Benutzeroberfläche definiert. D. h., möglicherweise zwei HRESULT-Werte mit genau die gleiche 32-Bit-Wert zurückgegeben von zwei verschiedenen Schnittstellen verschiedene Bedeutungen haben.  <br/> |
|FACILITY_DISPATCH  <br/> |Für späte Bindung [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) -Schnittstelle Fehler.  <br/> |
|FACILITY_RPC  <br/> |Für Statuscodes von Remoteprozeduraufrufe zurückgegeben.  <br/> |
|FACILITY_STORAGE  <br/> |Für Statuscodes [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) oder [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) Aufrufe von Methoden für strukturierte Speicher zurückgegeben. Statuscodes Code (unteren 16 Bit) Werte im Bereich von Windows-Fehlercodes (d. h., kleiner als 256) haben dieselbe Bedeutung wie die entsprechende Windows-Fehler.  <br/> |
   
Das Feld ist eine eindeutige Zahl, die zum Darstellen der Fehlermeldung oder einer Warnung zugewiesen ist.
  

