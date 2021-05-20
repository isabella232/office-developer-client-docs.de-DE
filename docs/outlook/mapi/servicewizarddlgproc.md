---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432380"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die vom Profil-Assistenten aufgerufen wird, damit ein Dienstanbieter auf Benutzerereignisse reagieren kann, wenn die Eigenschaftenblätter oder Seiten des Anbieters angezeigt werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI-Profil-Assistent  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

_hDlg_
  
> [in] Fensterhandle zum Dialogfeld Profil-Assistent. 
    
_wMsgID_
  
> [in] Die zu verarbeitende Fensternachricht. Zusätzlich zu den regulären Fenstermeldungen, die von einem modalen Dialogfeld erwartet werden, können die folgenden Nachrichten empfangen werden:
    
WM_CLOSE 
  
> Der Profil-Assistent wurde abgeschlossen. Der Dienstanbieter sollte alle erforderlichen Bereinigungen, z. B. die Zuweisung eines dynamisch zugewiesenen Arbeitsspeichers, tun. 
    
WM_COMMAND 
  
> Eines der Steuerelemente des Anbieters wurde ausgewählt,  oder auf die **Schaltfläche Weiter** oder Zurück wurde geklickt. Der Wert im  _wParam-Parameter_ gibt an, welches dieser Benutzerereignisse aufgetreten ist. 
    
WM_INITDIALOG 
  
> Der Benutzer wurde zu einer anderen Eigenschaftenseite verschoben, für die das Dialogfeld initialisiert werden muss. Der Anbieter sollte die Steuerelemente initialisieren, die der Profil-Assistent dem Dialogfeld hinzugefügt hat. 
    
WIZ_QUERYNUMPAGES 
  
> Der Profil-Assistent fordert die Anzahl der Seiten auf, die der Anbieter anzeigen muss. Der Anbieter sollte die Anzahl der Seiten anstelle von TRUE oder FALSE zurückgeben. Verwenden Sie beispielsweise die folgende Return-Anweisung, um anzugeben, dass drei Seiten angezeigt werden sollen:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> [in] Ein 32-Bit-Parameter, der Fenstermeldungen zugeordnet ist. Mögliche Werte hängen von der im  _wMsgID-Parameter angegebenen Nachricht_ ab. Zusätzlich zu den werten, die mit den regulären Fenstermeldungen für ein modales Dialogfeld erwartet werden, können die folgenden Werte empfangen werden: 
    
WIZ_NEXT 
  
> Wenn _wMsgID_ WM_COMMAND, hat der Benutzer auf die Schaltfläche **Weiter geklickt.** 
    
WIZ_PREV 
  
> Wenn _wMsgID_ WM_COMMAND, hat der Benutzer auf die Schaltfläche **Zurück geklickt.** 
    
_lParam_
  
> [in] Ein 32-Bit-Parameter, der Fenstermeldungen zugeordnet ist. Mögliche Werte hängen von der im  _wMsgID-Parameter angegebenen Nachricht_ ab. 
    
## <a name="return-value"></a>Rückgabewert

Der von einer **SERVICEWIZARDDLGPROC-basierten** Funktion zurückgegebene Wert hängt von der empfangenen Fensternachricht ab. Beachten Sie insbesondere den außergewöhnlichen Rückgabewert für die WIZ_QUERYNUMPAGES Nachricht. Die normalen Rückgabewerte sind: 
  
TRUE 
  
> Der Dienstanbieter hat die empfangene Fensternachricht verarbeitet. 
    
FALSE 
  
> Der Dienstanbieter hat die empfangene Fensternachricht nicht verarbeitet.
    
## <a name="remarks"></a>Hinweise

Wenn der Benutzer von einer Eigenschaftenseite zu einer anderen wechselt, ist der Anbieter dafür verantwortlich, die Steuerelemente der alten Seite zu ausblenden und die Steuerelemente für die nächste oder vorherige Seite zu zeigen. Wenn der Benutzer auf die **Schaltfläche Weiter** klickt, wird die **serviceWIZARDDLGPROC-basierte** Funktion mit der WM_COMMAND und WIZ_NEXT im  _wParam-Parameter_ aufgerufen. In den folgenden Schritten wird beschrieben, was zwischen dem Zeitpunkt, zu dem der Benutzer auf **Weiter** klickt, und dem Rendern der Konfigurationsseiten des ersten Anbieters geschieht. 
  
1. Der Profil-Assistent blendet alle Steuerelemente aus, die sich im Fenster befinden. 
    
2. Der Profil-Assistent fügt der Seite die ausgeblendeten Steuerelemente des Anbieters hinzu. 
    
3. Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC** auf und sendet die WM_INITDIALOG, damit der Anbieter die Steuerelemente initialisieren kann. 
    
4. Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC auf** und sendet WIZ_QUERYNUMPAGES Nachricht. Der Anbieter gibt die Anzahl der Seiten zurück, die angezeigt werden sollen. 
    
5. Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC** auf und sendet die WM_COMMAND-Nachricht, bei der der  _wParam-Parameter_ auf WIZ_NEXT oder WIZ_PREV. An diesem Punkt gibt der Anbieter entweder FALSE {error} zurück oder zeigt seine Steuerelemente an und gibt TRUE {success} zurück. Wenn der Profil-Assistent ID_NEXT, wird die erste Seite des Anbieters angezeigt. Wenn ID_PREV übergeben wird, wird die letzte Seite angezeigt. 
    
6. Der Profil-Assistent ruft die **SERVICEWIZARDDLGPROC-Funktion** des Anbieters auf und sendet die WM_COMMAND-Nachricht mit dem  _wParam-Parameter,_ der auf WIZ_NEXT oder WIZ_PREV festgelegt ist (je nachdem, auf welche Schaltfläche der Benutzer geklickt hat). Der Anbieter ist dafür verantwortlich, seine Steuerelemente ein- oder ausblenden und seine Daten in den **IMAPIProp** zu schreiben, der an den Profil-Assistenten übergeben wurde, um die Seitenabfolge zu durchblättern. Der Anbieter sollte TRUE zurückgeben, wenn die nächste oder vorherige Seite erfolgreich angezeigt wurde, und FALSE, wenn weder die nächste noch die vorherige Seite angezeigt werden konnte. Der Anbieter muss sich bewusst sein, wann er außerhalb seiner Seitenabfolge tritt, und entsprechend reagieren, indem er seine Steuerelemente ausblenden und seine Daten in das Profil schreibt. 
    
7. Wenn der Benutzer den Seitenbereich des Anbieters überschritt, löscht der Profil-Assistent die ausgeblendeten Steuerelemente des Anbieters aus dem Dialogfeld und ruft den nächsten Anbieter auf oder zeigt die nächste Seite an, wenn dies der letzte Anbieter war. 
    

