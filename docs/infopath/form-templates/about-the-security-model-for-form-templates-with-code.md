---
title: Informationen zum Sicherheitsmodell für Formularvorlagen mit Code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, Sicherheit, Codezugriffssicherheit [InfoPath 2007], [InfoPath 2007] Sicherheit, Sicherheitsmodell für verwalteten Code, Sicherheit [InfoPath 2007], Ebenen, CAS [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen, Sicherheit, Berechtigungen [InfoPath 2007]
localization_priority: Normal
ms.assetid: 5e1c1c72-f98d-4871-9c57-82c315277aa1
description: InfoPath-Formularvorlagen mit verwaltetem Code unterstützen dieselben Sicherheitsebenen wie Skript, das in unverwalteten Formularvorlagen ausgeführt wird. Außerdem werden zusätzliche Sicherheitsfeatures für den Codezugriff unterstützt, die auf verwalteten Code angewendet werden, der unter der Common Language Runtime (CLR) von .NET Framework ausgeführt wird.
ms.openlocfilehash: cfeb2117232d041cef43d282ff5aab482609f512
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790723"
---
# <a name="about-the-security-model-for-form-templates-with-code"></a>Informationen zum Sicherheitsmodell für Formularvorlagen mit Code

InfoPath-Formularvorlagen mit verwaltetem Code unterstützen dieselben Sicherheitsebenen wie Skript, das in unverwalteten Formularvorlagen ausgeführt wird. Außerdem werden zusätzliche Sicherheitsfeatures für den Codezugriff unterstützt, die auf verwalteten Code angewendet werden, der unter der Common Language Runtime (CLR) von .NET Framework ausgeführt wird.
  
## <a name="infopath-managed-object-model-security-levels"></a>Sicherheitsebenen des verwalteten InfoPath-Objektmodells

In der folgenden Tabelle wird die Beziehung zwischen den Sicherheitsebenen für Skriptobjekt-Modellmember und dem entsprechenden Berechtigungssatz beschrieben, der für die einzelnen Ebenen erforderlich ist, wenn der Objektmodellmember in einer Formularvorlage mit verwaltetem Code verwendet wird.
  
|**Sicherheitsebene des Objektmodells**|**Beschreibung**|**Erforderlicher Berechtigungssatz**|
|:-----|:-----|:-----|
|0  <br/> |Zugriff ohne Einschränkungen möglich  <br/> |Keiner  <br/> |
|2  <br/> |Zugriff nur möglich durch Formulare, die in derselben Domäne wie das zurzeit geöffnete Formular ausgeführt werden, oder durch Formulare, denen domänenübergreifende Berechtigungen gewährt wurden.  <br/> |Keiner  <br/> |
|3  <br/> |Zugriff nur durch voll vertrauenswürdige Formulare möglich.  <br/> |Voll vertrauenswürdig  <br/> |
   
> [!NOTE]
> Die Sicherheitsebene 1 wird nicht vom aktuellen InfoPath-COM-Server verwendet und ist für künftige Zwecke vorbehalten. 
  
> [!IMPORTANT]
> Obwohl die Objektmodellebenen 0 und 2 keinen Berechtigungssatz erfordern, da sie verwalteten Code enthalten, verhalten sie sich gemäß Definition für die Domänensicherheitsebene für den Domänenzugriff, die im folgenden Abschnitt beschrieben wird. 
  
Die Sicherheitsstufe der einzelnen Objektmodellelement durch die Microsoft.Office.InfoPath und Microsoft.Office.Interop.InfoPath.SemiTrust-Assembly verfügbar gemacht wird in Kommentarabschnitt des Themas angegeben, die diesen Member in der [Dokumente Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) und [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespaces. 
  
## <a name="infopath-domain-access-security-levels"></a>Sicherheitsebenen für den InfoPath-Domänenzugriff

Zusammen mit den Objektmodell-Sicherheitsebenen, die vom COM-Server erzwungen werden, der von der InfoPath-Anwendung verfügbar gemacht wird, werden von InfoPath drei Sicherheitsebenen definiert, deren Anwendung vom Speicherort der Formularvorlage, der Bereitstellungsart des Formulars und den im Entwurfsmodus konfigurierten Einstellungen abhängt. In der folgenden Tabelle sind diese drei Sicherheitsebenen definiert.
  
|**Domänenzugriffs-Sicherheitsebene**|**Beschreibung**|
|:-----|:-----|
|Eingeschränkt  <br/> |Kommunikation außerhalb der Formularvorlage ist nicht zulässig. Diese Sicherheitsstufe soll verhindern, dass schädliche Formulare Daten von Ihrem Computer an einen böswilligen Angreifer übertragen. Wenn in diesem Sicherheitsmodus ausgeführt wird, die folgenden Features funktionieren nicht: benutzerdefinierte Aufgabenbereich, Data Connections (mit Ausnahme der per e-Mail senden), ActiveX-Steuerelemente, verwaltetem Code Formularcode, Rollen und Workflows. Managed Code Form, die Vorlagen in der eingeschränkten Domäne nicht ausgeführt werden können. Wenn eine Formularvorlage verwalteten Code auf die Einstellung **Sicherheitsstufe automatisch ermitteln** , in der Kategorie **Sicherheit und Vertrauensstellung** des Dialogfeldes **Formularoptionen** festgelegt ist, erfordern die Formularvorlage immer mindestens den Domänenzugriff Sicherheit Ebene zum Ausführen von Code.  <br/><br/>**Wichtig**: die Assembly mit verwaltetem Code, die für eine Formularvorlage verwaltetem Code wird nicht geladen und ausgeführt wird, beim Öffnen eines Formulars aus einer eingeschränkten Domäne, z. B. von eines InfoPath-Formulars als e-Mail-Anlage gesendet wird erstellt. Jede Formularvorlage als e-Mail-Anlage bereitstellen möchten muss die oben aufgeführten Funktionen auslassen und wenn die Formularvorlage Formularcode enthält, Formularcode muss in JScript oder VBScript implementiert werden und muss nur Elemente des Objektmodells mit der Sicherheitsstufe 0 (null) verwenden .           |
|Domäne  <br/> |Beschränkt ein Formular anhand seines Speicherorts in einer der Sicherheitszonen, die von Microsoft Internet Explorer definiert wurden. Wenn sich das Formular z. B. in der Zone "Lokales Intranet" befindet, ist die Kommunikation mit anderen Daten innerhalb der eigenen Domäne zulässig. Das Abrufen von Daten aus anderen Domänen ist jedoch nicht zulässig. Durch den Speicherort in einer Sicherheitszone von Microsoft Internet Explorer wird außerdem festgelegt, ob ActiveX-Steuerelemente, die für Skripts als unsicher markiert sind, ausgeführt werden dürfen.  <br/> |
|Voll vertrauenswürdig  <br/> |Ermöglicht Ihnen das Ausführen eines Formulars mit voller Vertrauenswürdigkeit auf dem Computer, auf dem das Formular verwendet werden. Diese Sicherheitsstufe kann nur verwendet werden, bei der Arbeit mit einem Formular, die mit einer Signatur Digital, die mit einem vertrauenswürdigen Stammzertifizierungsstellen Herausgeber auf Ihrem Computer oder signiert ist durch die Erstellung einer Installationsprogramm, das das Formular installiert und legt die **RequireFullTrust** übereinstimmt -Attribut des **xDocumentClass** -Element auf "yes in der Formulardefinitionsdatei (XSF)". Mit dieser Einstellung Objektmodellaufrufe, die Sicherheitsstufe des Objektmodells 3, wie Eigenschaften und Methoden, die Zugriff auf das Dateisystem erfordern kann auf das Formular zugreifen, und Sie können bestimmte Sicherheitshinweise, die angezeigt werden, bei der Ausführung an einen restriktiveren Sicherheit deaktivieren die Ebene.  <br/> |
   
In der Standardeinstellung ein InfoPath-Formulars ist so konfiguriert, dass automatisch auswählen entweder die Sicherheitsstufe eingeschränkt oder Domäne Abhängigkeit von den Features, die verwendet werden, in der Formularvorlage, und wo und wie die Formularvorlage bereitgestellt wird. Eine Formularvorlage, die als e-Mail-Anlage bereitgestellt wird beispielsweise der eingeschränkten Sicherheitsstufe automatisch konfiguriert. Die Sicherheitsstufe ist immer restriktiv wie möglich, beginnend bei eingeschränkt, um einen höheren Grad an Sicherheit für Sie und Ihre Daten sicherzustellen. Wenn eine Formularvorlage mit verwaltetem Code, wählen Sie die Sicherheitsstufe automatisch festgelegt ist, wird die Formularvorlage immer mindestens mit der Domänensicherheitsstufe Zugriff müssen, bevor Code ausgeführt werden kann. Sie können diese Einstellung zur Entwurfszeit Auswahl ein Maß an Sicherheit, die für das Formular besser geeignet ist, mithilfe des folgenden Verfahrens manuell überschrieben. 
  
### <a name="specify-a-forms-security-level"></a>Angeben der Sicherheitsebene eines Formulars

1. Öffnen Sie das Formular im InfoPath-Formular-Designer, klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Info**, und klicken Sie dann auf **Formularoptionen**.
    
2. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung** . 
    
3. Löschen der **Sicherheitsstufe automatisch ermitteln (empfohlen)** das Kontrollkästchen. 
    
4. Wählen Sie die gewünschte Sicherheitsstufe aus.
    
> [!NOTE] 
> - Wenn Sie auswählen die **Eingeschränkte** Sicherheitsstufe für eine Formularvorlage verwaltetem Code, der Code-behind das Formular nicht geladen und ausgeführt werden werden Elemente des Objektmodells unabhängig von welchem-Objekt im Formularcode verwendet. Diese Sicherheitsstufe dient hauptsächlich für InfoPath-Formulare, die per e-Mail bereitgestellt werden.     
> - Wenn Sie die Sicherheitsstufe **Voll vertrauenswürdig** auswählen, müssen Sie digital signieren oder installieren und registrieren das Formular. Weitere Informationen finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md).
    
Die folgende Tabelle enthält eine Zusammenfassung des InfoPath-Sicherheitsmodells. In der ersten Spalte ist die Ebene aufgeführt, die für das Formular angegeben oder erforderlich ist. In der zweiten und dritten Spalte ist angegeben, ob das Formular über einen URN- oder URL-Bezeichner für den Speicherort verfügt. In den verbleibenden Spalten wird angegeben, was ausgeführt werden darf. Weitere Informationen zu Bereitstellungsszenarien und Berechtigungssätzen für Formularvorlagen mit verwaltetem Code finden Sie unter "Sicherheitsfeatures für den Common Language Runtime-Codezugriff" weiter unten in diesem Thema.
  
|**Formular erforderliche Ebene**|**Hat URN-Bezeichner**|**Hat URL-Bezeichner**|**ActiveX als unsicher für Skripts markiert**|**Domänenübergreifender Zugriff**|**Verwalteter code**|**Sicherheit des Objektmodells**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Eingeschränkt  <br/> ||X  <br/> |Kein ActiveX  <br/> |Fehler  <br/> |Formular wird geladen, aber verwalteter Code wird nicht ausgeführt  <br/> |0  <br/> |
|Domäne (Zone Internet Explorer **Eingeschränkte Sites** )  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |Wird nicht ausgeführt  <br/> |
|Domäne (Internet Explorer- **Internet** -Zone)  <br/> |X  <br/> ||Fehler  <br/> |Fehler  <br/> |Wird nicht ausgeführt  <br/> |0  <br/> |
|Domäne (Zone "Internet Explorer **Lokales Intranet** ")  <br/> |X  <br/> ||Fehler  <br/> |Eingabeaufforderung  <br/> |Verwalteter Code wird mit Berechtigungen für **Lokales Intranet** ausgeführt.  <br/> |2  <br/> |
|Domäne (Zone Internet Explorer **Vertrauenswürdige Sites** )  <br/> |X  <br/> ||Eingabeaufforderung  <br/> |OK  <br/> |Verwalteter Code ausgeführt wird, mit dem **Internet** Berechtigungen. Domänenübergreifender Zugriff ist zulässig. Beachten Sie, dass, obwohl das Formular in der Zone **Vertrauenswürdige Sites** befindet, **Internet** Berechtigungen angewendet werden.  <br/> |2  <br/> |
|Domäne (Internet Explorer **lokalen Computer** Zone)  <br/> |X  <br/> |X  <br/> |Eingabeaufforderung  <br/> |Fehler  <br/> |Verwalteter Code wird mit Berechtigungen für **Lokales Intranet** ausgeführt.  <br/> |2  <br/> |
|Voll vertrauenswürdig  <br/> |X  <br/> |X  <br/> |OK  <br/> |OK  <br/> |Voll vertrauenswürdig  <br/> |3  <br/> |
   
> [!IMPORTANT]
> Die Beschreibungen oben "markiert die ActiveX unsicher für Skripts" und "Cross-Domain-Zugriff" Spalten annehmen den Standardwert für Microsoft Internet Explorer-Sicherheitseinstellungen. Wenn ein Benutzer ihrer Sicherheitseinstellungen für die ändert, verhält InfoPath entsprechend anpassen. Angenommen, wenn in der Zone **Lokales Intranet** **auf Datenquellen über Domänengrenzen hinweg zugreifen** auf **Aktivieren**, festgelegt ist, und klicken Sie dann Benutzer nicht für den domänenübergreifenden Zugriff als aufgefordert werden beschrieben in der Tabelle. 
  
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
    
Informationen zum Erstellen und Konfigurieren der Codegruppe InfoPath-Formularvorlagen finden Sie unter [Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md).
  
Die folgende Tabelle enthält eine Zusammenfassung der Bereitstellungsszenarien und Berechtigungssätze, die auf Formularvorlagen mit verwaltetem Code angewendet werden.
  
|**Bereitstellungsszenario**|**Berechtigungssatz**|**Anmerkungen**|
|:-----|:-----|:-----|
|Die Formularvorlage wird auf dem lokalen Computer veröffentlicht, und der Entwickler verwendet Visual Studio, um Formularcode zu schreiben und zu debuggen.  <br/> |Berechtigungssatz "Lokales Intranet".  <br/> Assemblys im globalen Assemblycache (GAC) installiert und mit dem **AllowPartiallyTrustedCallersAttribute** -Attribut markiert werden den Berechtigungssatz voll vertrauenswürdig erteilt.  <br/> |Standardmäßig werden Formularvorlagen, die auf dem lokalen Computer ausgeführt nicht den Berechtigungssatz voll vertrauenswürdig erteilt. Während Sie beim Entwickeln von Formularvorlagen, die Features und Aufrufe-Objekts verwenden Mitglieder modellieren, die Berechtigungen für volle Vertrauenswürdigkeit erfordert, können Sie das in der [Vorschau und Debuggen von Formularvorlagen, erfordern voll vertrauenswürdig](how-to-preview-and-debug-form-templates-that-require-full-trust.md)beschriebene Verfahren verwenden.  <br/> |
|Die Formularvorlage wird auf dem lokalen Computer veröffentlicht und verweist auf eine benutzerdefinierte Assembly, für die die Berechtigung "Voll vertrauenswürdig" auf dem lokalen Computer erforderlich ist.  <br/> |Berechtigungssatz "Lokales Intranet".  <br/> Assemblys im globalen Assemblycache (GAC) installiert und mit dem **AllowPartiallyTrustedCallersAttribute** -Attribut markiert werden den Berechtigungssatz voll vertrauenswürdig erteilt. Die benutzerdefinierte Assembly erhält den Berechtigungssatz Lokales Intranet.  <br/> |Für den Verweis auf externe Assemblys zur Verwendung im Code der Formularvorlage muss der Entwickler die Codegruppe "InfoPath-Formularvorlagen" verwenden, um der externen Assembly, auf die im Code der Formularvorlage verwiesen wird, den vollständigen Zugriff (oder den entsprechenden Berechtigungssatz) zu gewähren. InfoPath trifft keine Annahmen über andere externe Assemblys als die, die im globalen Assemblycache (GAC) installiert sind. Der Entwickler muss der Assembly explizit die erforderlichen Berechtigungen mithilfe der Codegruppe "InfoPath-Formularvorlagen" gewähren, auch wenn die Assembly bereits durch Berechtigungen vertrauenswürdig gemacht wurde, die in der Codegruppe "Zone des lokalen Computers" gewährt wurden.  <br/> |
|Die Formularvorlage wird an einem freigegebenen Speicherort im lokalen Intranet veröffentlicht, z. B. auf einer Dateifreigabe, in einer SharePoint-Formularbibliothek oder auf einem Webserver.  <br/> |Berechtigungssatz "Lokales Intranet".  <br/> Assemblys im globalen Assemblycache (GAC) installiert und mit dem **AllowPartiallyTrustedCallersAttribute** -Attribut markiert werden den Berechtigungssatz voll vertrauenswürdig erteilt.  <br/> ||
|Die Formularvorlage wird an einem freigegebenen Speicherort im lokalen Intranet veröffentlicht, der in Internet Explorer als vertrauenswürdige Website definiert ist, z. B. auf einer Dateifreigabe, in einer SharePoint-Formularbibliothek oder auf einem Webserver.  <br/> |Berechtigungssatz "Internet".  <br/> Von Microsoft und ECMA signierten Assemblys wird die Berechtigung "Voll vertrauenswürdig" gewährt.  <br/> |Durch die CLR-Codezugriffssicherheit wird der Berechtigungssatz "Internet" nur für Websites gewährt, die in Internet Explorer als vertrauenswürdige Websites definiert sind. InfoPath berücksichtigt diese Richtlinie. Möglicherweise wird von einer InfoPath-Formularvorlage Skript für Formularcode nicht verwendet, da diese beim Veröffentlichen in einer Zone vertrauenswürdiger Websites eine höhere Berechtigungsebene erhält.   <br/> |
|Die Formularvorlage wird von einem Speicherort im Internet gedownloadet oder kopiert.  <br/> |Standardmäßig keine. Die Assembly mit verwaltetem Code für die Formularvorlage wird nicht geladen und nicht ausgeführt.  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md)
- [Anzeigen der Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

