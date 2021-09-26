---
title: Informationen zum Sicherheitsmodell für Formularvorlagen mit Code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, security,code access security [InfoPath 2007],security [InfoPath 2007], security model for managed code,security [InfoPath 2007], levels,CAS [InfoPath 2007],InfoPath 2003-compatible form templates, security,permissions [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 5e1c1c72-f98d-4871-9c57-82c315277aa1
description: InfoPath-Formularvorlagen mit verwaltetem Code unterstützen dieselben Sicherheitsebenen wie Skript, das in unverwalteten Formularvorlagen ausgeführt wird. Außerdem werden zusätzliche Sicherheitsfeatures für den Codezugriff unterstützt, die auf verwalteten Code angewendet werden, der unter der Common Language Runtime (CLR) von .NET Framework ausgeführt wird.
ms.openlocfilehash: 97735f0f707cc73d86b313b5aaac2758de71a5f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631384"
---
# <a name="about-the-security-model-for-form-templates-with-code"></a>Informationen zum Sicherheitsmodell für Formularvorlagen mit Code

InfoPath-Formularvorlagen mit verwaltetem Code unterstützen dieselben Sicherheitsebenen wie Skript, das in unverwalteten Formularvorlagen ausgeführt wird. Außerdem werden zusätzliche Sicherheitsfeatures für den Codezugriff unterstützt, die auf verwalteten Code angewendet werden, der unter der Common Language Runtime (CLR) von .NET Framework ausgeführt wird.
  
## <a name="infopath-managed-object-model-security-levels"></a>Sicherheitsebenen des verwalteten InfoPath-Objektmodells

In der folgenden Tabelle wird die Beziehung zwischen den Sicherheitsebenen für Skriptobjekt-Modellmember und dem entsprechenden Berechtigungssatz beschrieben, der für die einzelnen Ebenen erforderlich ist, wenn der Objektmodellmember in einer Formularvorlage mit verwaltetem Code verwendet wird.
  
|**Sicherheitsstufe des Objektmodells**|**Beschreibung**|**Erforderlicher Berechtigungssatz**|
|:-----|:-----|:-----|
|0  <br/> |Zugriff ohne Einschränkungen möglich  <br/> |Keines  <br/> |
|2  <br/> |Zugriff nur möglich durch Formulare, die in derselben Domäne wie das zurzeit geöffnete Formular ausgeführt werden, oder durch Formulare, denen domänenübergreifende Berechtigungen gewährt wurden.  <br/> |Keines  <br/> |
|3  <br/> |Zugriff nur durch voll vertrauenswürdige Formulare möglich.  <br/> |Fulltrust  <br/> |
   
> [!NOTE]
> Die Sicherheitsebene 1 wird nicht vom aktuellen InfoPath-COM-Server verwendet und ist für künftige Zwecke vorbehalten. 
  
> [!IMPORTANT]
> Obwohl die Objektmodellebenen 0 und 2 keinen Berechtigungssatz erfordern, da sie verwalteten Code enthalten, verhalten sie sich gemäß Definition für die Domänensicherheitsebene für den Domänenzugriff, die im folgenden Abschnitt beschrieben wird. 
  
Die Sicherheitsstufe der einzelnen Objektmodellmember, die von Microsoft verfügbar gemacht werden. Office. InfoPath und Microsoft. Office.Interop.InfoPath.SemiTrust assemblies is specified in the Remarks section of the topic that documents that member in the [Microsoft.Office. InfoPath-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) und [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespaces.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 
  
## <a name="infopath-domain-access-security-levels"></a>Sicherheitsebenen für den InfoPath-Domänenzugriff

Zusammen mit den Objektmodell-Sicherheitsebenen, die vom COM-Server erzwungen werden, der von der InfoPath-Anwendung verfügbar gemacht wird, werden von InfoPath drei Sicherheitsebenen definiert, deren Anwendung vom Speicherort der Formularvorlage, der Bereitstellungsart des Formulars und den im Entwurfsmodus konfigurierten Einstellungen abhängt. In der folgenden Tabelle sind diese drei Sicherheitsebenen definiert.
  
|**Domänenzugriffs-Sicherheitsebene**|**Beschreibung**|
|:-----|:-----|
|Eingeschränkt  <br/> |Außerhalb der Formularvorlage ist keine Kommunikation zulässig. Diese Sicherheitsebene soll verhindern, dass gefährliche Formulare Daten von Ihrem Computer an gefährliche Angreifer übertragen. Wenn sie in diesem Sicherheitsmodus ausgeführt werden, funktionieren die folgenden Features nicht: benutzerdefinierter Aufgabenbereich, Datenverbindungen (außer E-Mail-Übermittlung), ActiveX Steuerelemente, Formularcode mit verwaltetem Code, Rollen und Workflow. Formularvorlagen mit verwaltetem Code können nicht in der eingeschränkten Domäne ausgeführt werden. Wenn für eine Formularvorlage mit verwaltetem Code die Einstellung **Sicherheitsstufe automatisch ermitteln** in der Kategorie **Sicherheit und Vertrauensstellung** im Dialogfeld **Formularoptionen** festgelegt ist, ist für die Formularvorlage immer mindestens die Domänensicherheitsebene für den Zugriff erforderlich, um Code auszuführen.  <br/><br/>**WICHTIG:** Die assembly mit verwaltetem Code, die für eine Formularvorlage mit verwaltetem Code erstellt wurde, wird nicht geladen und nicht ausgeführt, wenn ein Formular aus einer eingeschränkten Domäne geöffnet wird, z. B. aus einem InfoPath-Formular, das als E-Mail-Anlage gesendet wird. Jede Formularvorlage, die Sie als E-Mail-Anlage bereitstellen möchten, muss die oben aufgeführten Features weglassen. Wenn die Formularvorlage Formularcode enthält, muss Formularcode in JScript oder VBScript implementiert werden und darf nur Objektmodellmember mit der Sicherheitsstufe 0 (null) verwenden.           |
|Domäne  <br/> |Beschränkt ein Formular anhand seines Speicherorts in einer der Sicherheitszonen, die von Microsoft Internet Explorer definiert wurden. Wenn sich das Formular z. B. in der Zone "Lokales Intranet" befindet, ist die Kommunikation mit anderen Daten innerhalb der eigenen Domäne zulässig. Das Abrufen von Daten aus anderen Domänen ist jedoch nicht zulässig. Durch den Speicherort in einer Sicherheitszone von Microsoft Internet Explorer wird außerdem festgelegt, ob ActiveX-Steuerelemente, die für Skripts als unsicher markiert sind, ausgeführt werden dürfen.  <br/> |
|Voll vertrauenswürdig  <br/> |Ermöglicht das Ausführen eines Formulars mit vollständiger Vertrauenswürdigkeit auf dem Computer, auf dem das Formular verwendet wird. Diese Sicherheitsebene kann nur beim Arbeiten mit einem Formular verwendet werden, das digital mit einer Signatur signiert wurde, die mit einem vertrauenswürdigen Stammherausgeber auf Ihrem Computer übereinstimmt, oder durch Erstellen eines Installationsprogramms, mit dem das Formular installiert und für das **requireFullTrust**-Attribut des **xDocumentClass**-Elements der Wert "yes" in der Formulardefinitionsdatei (XSF) festgelegt wird. Durch Verwenden dieser Einstellung kann das Formular auf Objektmodellaufrufe zugreifen, für die die Objektmodell-Sicherheitsebene 3 erforderlich ist, z. B. Eigenschaften und Methoden, die auf das Dateisystem zugreifen. Sie können außerdem bestimmte Sicherheitsaufforderungen deaktivieren, die bei der Ausführung auf einer restriktiveren Sicherheitsebene angezeigt werden. <br/> |
   
Standardmäßig ist ein InfoPath-Formular so konfiguriert, dass die Sicherheitsstufe "Eingeschränkt" oder "Domäne" automatisch ausgewählt wird, je nachdem, welche Features in der Formularvorlage verwendet werden und wo und wie die Formularvorlage bereitgestellt wird. Beispielsweise wird eine als E-Mail-Anlage bereitgestellte Formularvorlage automatisch auf die Sicherheitsstufe "Eingeschränkt" konfiguriert. Die Sicherheitseinstellung ist immer so restriktiv wie möglich, beginnend bei Restricted, um ein höheres Schutzniveau für Sie und Ihre Daten sicherzustellen. Wenn eine Formularvorlage, die verwalteten Code enthält, so festgelegt ist, dass automatisch die Sicherheitsstufe ausgewählt wird, erfordert die Formularvorlage mindestens die Domänensicherheitszugriffsebene, bevor Code ausgeführt werden kann. Mit dem folgenden Verfahren können Sie diese Einstellung zur Entwurfszeit manuell überschreiben, um eine sicherheitsebene auszuwählen, die für das Formular besser geeignet ist. 
  
### <a name="specify-a-forms-security-level"></a>Angeben der Sicherheitsebene eines Formulars

1. Öffnen Sie das Formular im InfoPath-Formular-Designer, klicken Sie auf die Registerkarte **Datei**, klicken Sie auf **Info**, und klicken Sie dann auf **Formularoptionen**.
    
2. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung**. 
    
3. Deaktivieren Sie das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln (empfohlen)**. 
    
4. Wählen Sie die gewünschte Sicherheitsebene aus.
    
> [!NOTE] 
> - Wenn Sie für eine Formularvorlage mit verwaltetem Code die Sicherheitsebene **Eingeschränkt** auswählen, wird der Code hinter dem Formular nicht geladen oder ausgeführt, unabhängig von den im Formularcode verwendeten Objektmodellmembern. Diese Sicherheitsstufe ist in erster Linie für InfoPath-Formulare konzipiert, die per E-Mail bereitgestellt werden.     
> - Wenn Sie die Sicherheitsebene **Voll vertrauenswürdig** auswählen, müssen Sie das Formular digital signieren oder installieren und registrieren. Weitere Informationen finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code.](how-to-deploy-infopath-form-templates-with-code.md)
    
Die folgende Tabelle enthält eine Zusammenfassung des InfoPath-Sicherheitsmodells. In der ersten Spalte ist die Ebene aufgeführt, die für das Formular angegeben oder erforderlich ist. In der zweiten und dritten Spalte ist angegeben, ob das Formular über einen URN- oder URL-Bezeichner für den Speicherort verfügt. In den verbleibenden Spalten wird angegeben, was ausgeführt werden darf. Weitere Informationen zu Bereitstellungsszenarien und Berechtigungssätzen für Formularvorlagen mit verwaltetem Code finden Sie unter "Sicherheitsfeatures für den Common Language Runtime-Codezugriff" weiter unten in diesem Thema.
  
|**Für das Formular erforderliche Ebene**|**Hat URN-Bezeichner**|**Hat URL-Bezeichner**|**ActiveX als unsicher für Skripting gekennzeichnet**|**Domänenübergreifender Zugriff**|**Verwalteter Code**|**Objektmodellsicherheit**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Eingeschränkt  <br/> ||X  <br/> |Kein ActiveX  <br/> |Fehler  <br/> |Formular wird geladen, aber verwalteter Code wird nicht ausgeführt  <br/> |0  <br/> |
|Domäne (Internet Explorer-Zone **Eingeschränkte Sites**)  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |
|Domäne (Internet Explorer-Zone **Internet**)  <br/> |X  <br/> ||Fehler  <br/> |Fehler  <br/> |Wird nicht ausgeführt  <br/> |0  <br/> |
|Domäne (Internet Explorer-Zone für **Lokales Intranet**)  <br/> |X  <br/> ||Fehler  <br/> |Eingabeaufforderung  <br/> |Verwalteter Code wird mit Berechtigungen für **Lokales Intranet** ausgeführt.  <br/> |2  <br/> |
|Domäne (Internet Explorer-Zone **Vertrauenswürdige Sites**)  <br/> |X  <br/> ||Eingabeaufforderung  <br/> |OK  <br/> |Verwalteter Code wird mit den Berechtigungen **Internet** ausgeführt. Domänenübergreifender Zugriff ist zulässig. Beachten Sie, dass obwohl sich das Formular in der Sicherheitszone **Vertrauenswürdige Sites** befindet, die Sicherheitszonenberechtigungen **Internet** angewendet werden.<br/> |2  <br/> |
|Domäne (Internet Explorer-Zone **Lokaler Computer**)  <br/> |X  <br/> |X  <br/> |Eingabeaufforderung  <br/> |Fehler  <br/> |Verwalteter Code wird mit Berechtigungen für **Lokales Intranet** ausgeführt.  <br/> |2  <br/> |
|Voll vertrauenswürdig  <br/> |X  <br/> |X  <br/> |OK  <br/> |OK  <br/> |Voll vertrauenswürdig  <br/> |3  <br/> |
   
> [!IMPORTANT]
> Bei den oben genannten Beschreibungen in den Spalten "ActiveX als unsicher für Skripts markiert" und "Domänenübergreifender Zugriff" wird von den Standardsicherheitseinstellungen für Microsoft Internet Explorer ausgegangen. Wenn ein Benutzer die Sicherheitseinstellungen ändert, ist das Verhalten von InfoPath entsprechend. Wenn z. B. in der Zone **Lokales Intranet** für **Auf Datenquellen über Domänengrenzen hinweg zugreifen** die Einstellung **Aktivieren** festgelegt ist, werden Benutzer nicht aufgefordert, den domänenübergreifenden Zugriff gemäß Beschreibung in der Tabelle zuzulassen. 
  
## <a name="common-language-runtime-code-access-security-features"></a>Sicherheitsfeatures für den Common Language Runtime-Codezugriff

Beim Kompilieren einer InfoPath-Formularvorlage mit verwaltetem Code wird eine private Assembly mit verwaltetem Code erstellt, in der die Implementierung der Formularcodelogik enthalten ist.
  
In .NET Framework hat eine Assembly mit verwaltetem Code standardmäßig beim Ausführen auf dem lokalen Computer die Berechtigung "Voll vertrauenswürdig". Beim Ausführen im Intranet wird die Berechtigung "Voll vertrauenswürdig" nicht gewährt. Von InfoPath wird die folgende Sicherheitsarchitektur implementiert, um eine besser abgestimmte Steuerung über Sicherheitsrichtlinien und die Option zum Ausführen von InfoPath-Formularvorlagen mit verwaltetem Code als voll vertrauenswürdige Formulare aus dem Intranet bereitzustellen.
  
- Die InfoPath-Anwendung hostet die .NET Framework Common Language Runtime (CLR).
    
- In der von InfoPath gehosteten CLR wird jede Formularvorlage mit verwaltetem Code in einer getrennten Anwendungsdomäne ausgeführt. Dabei handelt es sich um eine Umgebung, die Isolation, Entladung und Sicherheitsbegrenzungen zum Ausführen von verwaltetem Code bereitstellt.
    
- InfoPath legt für die Anwendungsdomäne eine Standardsicherheitsrichtlinie fest, je nach Vertrauensebene, die der Formularvorlage und dem URL des Speicherorts zugeordnet ist.
    
- Standardmäßig erhält eine Formularvorlage mit verwaltetem Code, die auf dem lokalen Computer ausgeführt wird (Codegruppe "Zone des lokalen Computers"), eine niedrigere Berechtigungsebene als "Voll vertrauenswürdig" (Berechtigungssatz "Zone für lokales Intranet"). Für die Berechtigung "Voll vertrauenswürdig" muss das Formular mit einem vertrauenswürdigen Zertifikat digital signiert oder registriert werden.
    
Durch den standardmäßigen Sicherheitsrichtliniensatz für die Anwendungsdomäne einer Formularvorlage mit verwaltetem Code wird sichergestellt, dass die Sicherheitsebenen für den InfoPath-Domänenzugriff sowie zusätzliche .NET-Sicherheitseinschränkungen erzwungen werden. Das InfoPath-Sicherheitssystem erkennt eine Codegruppe für die .NET-Codezugriffssicherheit namens "InfoPath-Formularvorlagen", um zusätzliche Flexibilität bereitzustellen. Wenn diese Codegruppe auf dem Computer eines Benutzers vorhanden ist, werden ihre Sicherheitskonfiguration und die Sicherheitskonfigurationen ggf. vorhandener untergeordneter Codegruppen auf die Anwendungsdomäne angewendet.
  
> [!IMPORTANT] 
> - Die Codegruppe "InfoPath-Formularvorlagen" wird nur auf die Formularcodeassembly mit verwaltetem Code angewendet. Daher verursachen Aufrufe im Formularcode für Objektmodellmember der Sicherheitsebene 3 weiterhin Fehler, wenn Sie Infopath-Formularcode mit verwaltetem Code die Berechtigung "Voll vertrauenswürdig" gewähren, aber die Formularvorlage nicht installiert und registriert (bzw. digital signiert) haben (wodurch die gesamte Formularvorlage voll vertrauenswürdig wird).    
> - Wenn Sie auf eine Assembly verweisen oder sie explizit laden (Assembly.Load), die mit einem eingeschränkten Berechtigungssatz konfiguriert ist, wobei mithilfe der Beweise "Hash", "Starker Name" oder "Herausgeber" die Mitgliedschaftsbedingung in einem Formularvorlagenprojekt bestimmt wird, wird die Assembly trotzdem geladen und von der Formularvorlage ausgeführt.
    
Informationen zum Erstellen und Konfigurieren der Codegruppe InfoPath-Formularvorlagen finden Sie unter Konfigurieren von [Sicherheits-Einstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md).
  
Die folgende Tabelle enthält eine Zusammenfassung der Bereitstellungsszenarien und Berechtigungssätze, die auf Formularvorlagen mit verwaltetem Code angewendet werden.
  
|**Bereitstellungsszenario**|**Berechtigungssatz**|**Hinweise**|
|:-----|:-----|:-----|
|Die Formularvorlage wird auf dem lokalen Computer veröffentlicht, und der Entwickler verwendet Visual Studio, um Formularcode zu schreiben und zu debuggen.  <br/> |Berechtigungssatz "Lokales Intranet".  <br/> Assemblys, die im globalen Assemblycache (GAC) installiert und mit dem **AllowPartiallyTrustedCallersAttribute**-Attribut markiert sind, wird die Berechtigung "Voll vertrauenswürdig" gewährt.  <br/> |Standardmäßig wird Formularvorlagen, die vom lokalen Computer ausgeführt werden, nicht die Berechtigung "Voll vertrauenswürdig" gewährt. Beim Entwickeln von Formularvorlagen, die Features und Aufrufe von Objektmodellmembern verwenden, für die Voll vertrauenswürdige Berechtigungen erforderlich sind, können Sie die unter ["Vorschau" und "Debuggen von Formularvorlagen"](how-to-preview-and-debug-form-templates-that-require-full-trust.md)beschriebene Prozedur verwenden, die voll vertrauenswürdig ist.  <br/> |
|Die Formularvorlage wird auf dem lokalen Computer veröffentlicht und verweist auf eine benutzerdefinierte Assembly, für die die Berechtigung "Voll vertrauenswürdig" auf dem lokalen Computer erforderlich ist.  <br/> |Berechtigungssatz "Lokales Intranet".  <br/> Assemblys, die im globalen Assemblycache (GAC) installiert und mit dem **AllowPartiallyTrustedCallersAttribute**-Attribut markiert sind, wird die Berechtigung "Voll vertrauenswürdig" gewährt. Der benutzerdefinierten Assembly wird der Berechtigungssatz "Lokales Intranet" gewährt.<br/> |Für den Verweis auf externe Assemblys zur Verwendung im Code der Formularvorlage muss der Entwickler die Codegruppe "InfoPath-Formularvorlagen" verwenden, um der externen Assembly, auf die im Code der Formularvorlage verwiesen wird, den vollständigen Zugriff (oder den entsprechenden Berechtigungssatz) zu gewähren. InfoPath trifft keine Annahmen über andere externe Assemblys als die, die im globalen Assemblycache (GAC) installiert sind. Der Entwickler muss der Assembly explizit die erforderlichen Berechtigungen mithilfe der Codegruppe "InfoPath-Formularvorlagen" gewähren, auch wenn die Assembly bereits durch Berechtigungen vertrauenswürdig gemacht wurde, die in der Codegruppe "Zone des lokalen Computers" gewährt wurden.  <br/> |
|Die Formularvorlage wird an einem freigegebenen Speicherort im lokalen Intranet veröffentlicht, z. B. auf einer Dateifreigabe, in einer SharePoint-Formularbibliothek oder auf einem Webserver.  <br/> |Berechtigungssatz "Lokales Intranet".  <br/> Assemblys, die im globalen Assemblycache (GAC) installiert und mit dem **AllowPartiallyTrustedCallersAttribute**-Attribut markiert sind, wird die Berechtigung "Voll vertrauenswürdig" gewährt.  <br/> ||
|Die Formularvorlage wird an einem freigegebenen Speicherort im lokalen Intranet veröffentlicht, der in Internet Explorer als vertrauenswürdige Website definiert ist, z. B. auf einer Dateifreigabe, in einer SharePoint-Formularbibliothek oder auf einem Webserver.  <br/> |Berechtigungssatz "Internet".  <br/> Von Microsoft und ECMA signierten Assemblys wird die Berechtigung "Voll vertrauenswürdig" gewährt.  <br/> |Durch die CLR-Codezugriffssicherheit wird der Berechtigungssatz "Internet" nur für Websites gewährt, die in Internet Explorer als vertrauenswürdige Websites definiert sind. InfoPath berücksichtigt diese Richtlinie. Möglicherweise wird von einer InfoPath-Formularvorlage Skript für Formularcode nicht verwendet, da diese beim Veröffentlichen in einer Zone vertrauenswürdiger Websites eine höhere Berechtigungsebene erhält.   <br/> |
|Die Formularvorlage wird von einem Speicherort im Internet gedownloadet oder kopiert.  <br/> |Standardmäßig keine. Die Assembly mit verwaltetem Code für die Formularvorlage wird nicht geladen und nicht ausgeführt.  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [Konfigurieren von Sicherheits-Einstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md)
- [Anzeigen einer Vorschau und Debuggen von Formularvorlagen, die vollständig vertrauenswürdig sein müssen](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

