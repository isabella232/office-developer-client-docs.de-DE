---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ed35eabe27223d8c2af6be0a30e6ec678c0dfc8a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584192"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Funktion, die die Profil-Assistent-Anwendung zum Hinzufügen eines oder mehrerer Nachrichtendienste zu einem Profil startet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |MAPI  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a>Parameter

 _hParentWnd_
  
> [in] Ein Handle für das übergeordnete Fenster des Aufrufers. Wenn der Aufrufer kein übergeordnetes Fenster hat, sollte der  _Parameter hParentWnd_ NULL sein. 
    
 _ulFlags_
  
> [in] Bitmaske mit Flags, die Optionen für den Profil-Assistenten angeben. Die folgenden Flags können festgelegt werden:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> Der Profil-Assistent soll nur die Nachrichtendienste hinzufügen, die über den  _LppszServiceNameToAdd-Parameter_ aufgelistet sind, und seine Seite zum Auswählen von Nachrichtendiensten nicht anzeigen. 
    
MAPI_PW_FIRST_PROFILE 
  
> Das zu erstellende Profil ist das erste Profil für diese Arbeitsstation. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> Die Seite des Profil-Assistenten zum Auswählen von Nachrichtendiensten sollte nicht angezeigt werden. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> Der Profil-Assistent wurde von der Systemsteuerungskonfigurationsanwendung gestartet. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Nur die Konfigurationsdialogfelder des Dienstanbieters sollten angezeigt werden, und die Seiten des Profil-Assistenten sollten nicht angezeigt werden. Dieses Flag kann nur festgelegt werden, wenn das MAPI_PW_ADD_SERVICE_ONLY-Flag festgelegt ist. 
    
 _lppszServiceNameToAdd_
  
> [in] Zeiger auf ein Zeichenfolgenarray, das die Namen der Nachrichtendienste enthält, die dem Profil hinzugefügt werden sollen. Das Array muss mit einem NULL-Wert beendet werden. 
    
 _cbBufferMax_
  
> [in] Größe des Puffers, auf den der  _parameter lpszNewProfileName_ verweist. 
    
 _lpszNewProfileName_
  
> [out] Zeiger auf einen Zeichenfolgenpuffer, in dem die auf **LAUNCHWIZARDENTRY** basierende Funktion den Namen des erstellten Profils zurückgibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte, dass der Vorgang abgeschlossen wurde. Mögliche Möglichkeiten sind das Fehlschlagen der Initialisierung des MAPI-Subsystems für den Profil-Assistenten, die Unfähigkeit, auf das Standardprofil zuzugreifen, und eine Fehlerrückgabe aus dem Dialogfeld.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die MAPI-Implementierung des **LaunchWIZARDENTRY-Funktionsprototyps** ist der Einstiegspunkt in die MAPI-Profil-Assistent-Anwendung. MAPI benennt diesen Einstiegspunkt **LaunchWizard**. 
  
Wenn das flag MAPI_PW_ADD_SERVICE_ONLY im  _ulFlags-Parameter_ festgelegt ist, gelten die folgenden Regeln: 
  
- Das MAPI_PW_LAUNCHED_BY_CONFIG Flag verhindert, dass die Willkommensseite angezeigt wird. 
    
- Die Flags MAPI_PW_HIDE_SERVICES_LIST und MAPI_PW_PROVIDER_UI_ONLY sind nur nützlich, wenn kein Standardprofil vorhanden ist. In diesem Fall bestimmen diese Flags, welche Seite des Profil-Assistenten angezeigt werden soll. 
    
- Wenn ein Standardprofil vorhanden ist, werden keine Seiten des Profil-Assistenten angezeigt. 
    
- Wenn ein Standardprofil vorhanden ist, wird nur ein Nachrichtendienst über den  _LppszServiceNameToAdd-Parameter_ aufgelistet, und dieser Nachrichtendienst befindet sich bereits im Standardprofil, der Profil-Assistent gibt S_OK zurück, ohne dem Profil etwas hinzuzufügen. 
    
Für jeden Nachrichtendienst, der dem Profil hinzugefügt werden soll, ruft der Profil-Assistent die Einstiegspunktfunktion des Diensts basierend auf dem [MSGSERVICEENTRY-Prototyp](msgserviceentry.md) auf. Für jeden Dienstanbieter, der aus einem Nachrichtendienst ausgewählt wurde, der dem Profil hinzugefügt werden soll, ruft der Profil-Assistent die Einstiegspunktfunktion des Anbieters basierend auf dem [WIZARDENTRY-Prototyp](wizardentry.md) auf. Während der interaktiven Konfiguration bewirkt jedes Benutzerereignis auf den Eigenschaftenseiten, dass der Profil-Assistent die Rückruffunktion des Anbieters basierend auf dem [SERVICEWIZARDDLGP PROTOTYPING-Prototyp](servicewizarddlgproc.md) aufruft. 
  
Wenn ein Dienstanbieter, der dem Profil hinzugefügt wird, die Seiten des Profil-Assistenten unterstützt, muss die programmgesteuerte Konfiguration des Profils zulässig sein.
  

