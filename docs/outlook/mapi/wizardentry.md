---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1a61d77c98766acf57bdb24865624023e0145557
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629445"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Dienstanbieter-Einstiegspunktfunktion, die der Profil-Assistent aufruft, um genügend Informationen zum Anzeigen der Konfigurationseigenschaftenblätter des Anbieters abzurufen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI-Profil-Assistent  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a>Parameter

 _hProviderDLLInstance_
  
> [in] Instanzhandle der DLL des Dienstanbieters. 
    
 _lpcsResourceName_
  
> [out] Zeiger auf eine Zeichenfolge, die den vollständigen Namen der Dialogressource enthält, die während der Konfiguration vom Profil-Assistenten angezeigt werden soll. Die maximale Größe der Zeichenfolge, einschließlich des NULL-Abschlusszeichens, beträgt 32 Zeichen. 
    
 _lppDlgProc_
  
> [out] Zeiger auf eine standardmäßige Windows Dialogfeldprozedur, die vom Profil-Assistenten aufgerufen wird, um den Anbieter über verschiedene Ereignisse zu benachrichtigen. 
    
 _lpMAPIProp_
  
> [in] Zeiger auf eine Implementierung der Eigenschaftenschnittstelle, die Zugriff auf die Konfigurationseigenschaften bietet. 
    
 _lpMapiSupportObject_
  
> [in] Zeiger auf das MAPI-Unterstützungsobjekt, das für diese Sitzung gilt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die **WIZARDENTRY-Funktion** des Dienstanbieters wurde erfolgreich aufgerufen. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte, dass der Vorgang abgeschlossen wurde.
    
## <a name="remarks"></a>Bemerkungen

Der Profil-Assistent ruft die **WIZARDENTRY-basierte** Funktion auf, wenn sie bereit ist, die Konfigurations-Benutzeroberfläche des Dienstanbieters anzuzeigen. Wenn der Profil-Assistent alle Anbieter konfiguriert hat, werden die Konfigurationseigenschaften in das Profil geschrieben, indem [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)aufgerufen wird. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Name der **WIZARDENTRY-basierten** Funktion muss im WIZARD_ENTRY_NAME Eintrag in MAPISVC.INF platziert werden. 
  
Der Ressourcenname ist der Name der Dialogressource, die im Bereich des Profil-Assistenten gerendert wird. Die ressource, die übergeben wird, muss alle Seiten in einer einzelnen Dialogressource enthalten. Wenn der Profil-Assistent diese Ressource empfängt, ignoriert er die Dialogformatvorlage, aber nicht die Steuerelementstile und erstellt alle Steuerelemente als untergeordnete Elemente der Seite des Profil-Assistenten. Alle Steuerelemente werden anfänglich ausgeblendet. Anbieter sollten sicherstellen, dass die Koordinaten für ihre Steuerelemente null- oder nullbasiert sind und eine maximale Breite von 200 Dialogfeldeinheiten und eine maximale Höhe von 150 Dialogfeldeinheiten nicht überschreiten. Steuerelement-IDs unter 400 sind für den Profil-Assistenten reserviert. Der Profil-Assistent zeigt den Titel des Anbieters in fettem Text über der Benutzeroberfläche des Anbieters an. 
  
Der im  _lpMAPIProp-Parameter_ angegebene Eigenschaftenschnittstellenzeiger sollte vom Anbieter für zukünftige Verweise beibehalten werden. Der Profil-Assistent behandelt nur den grundlegendsten Satz von Eigenschaften, und der Anbieter kann die Implementierung der Eigenschaftenschnittstelle verwenden, um zusätzliche Eigenschaften einzuschließen. Während der Konfiguration sollten Anbieter ihre Konfigurationseigenschaften dem Objekt hinzufügen, das die Eigenschaftenschnittstelle implementiert. Nachdem alle Anbieter konfiguriert wurden, fügt der Profil-Assistent diese Eigenschaften zum Profil hinzu. 
  
Weitere Informationen zur Verwendung dieser Funktion finden Sie unter Unterstützen der [Nachrichtendienstkonfiguration.](supporting-message-service-configuration.md) 
  

