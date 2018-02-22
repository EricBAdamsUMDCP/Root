# Root
A log of code and notes for using root in the Mignerey lab
undeclared identifier 'c1'
TCanvas* c1 = new TCanvas();
TCanvas* c1;

{
   c1 = new TCanvas()
}
{
...

  c1 = new TCanvas();
  histogram_1D->SetXTitle("ETsum");
  histogram_1D->SetYTitle("counts");
  c1->SetLogy();
  gStyle->SetOptLogz();
  gStyle->SetOptFit();
  histogram_1D->Draw();
 
  c2 = new TCanvas();
  histogram_2D->SetXTitle("ETsum (fC)");
  histogram_2D->SetYTitle("EMsum (fC)"); 
  gStyle->SetPalette(1);
  gStyle->SetOptLogz();
  histogram_2D->Draw("colz");
 
 
}
{
...

  TCanvas* c1 = new TCanvas();
  histogram_1D->SetXTitle("ETsum");
  histogram_1D->SetYTitle("counts");
  c1->SetLogy();
  gStyle->SetOptLogz();
  gStyle->SetOptFit();
  histogram_1D->Draw();
 
 TCanvas* c2 = new TCanvas();
  histogram_2D->SetXTitle("ETsum (fC)");
  histogram_2D->SetYTitle("EMsum (fC)"); 
  gStyle->SetPalette(1);
  gStyle->SetOptLogz();
  histogram_2D->Draw("colz");
 
 
}
{
...

  TCanvas* c1 = new TCanvas();
  histogram_1D->SetXTitle("ETsum");
  histogram_1D->SetYTitle("counts");
  c1->SetLogy();
  gStyle->SetOptLogz();
  gStyle->SetOptFit();
  histogram_1D->Draw();
  delete c1; // fixes mem leak
 
 TCanvas* c2 = new TCanvas();
  histogram_2D->SetXTitle("ETsum (fC)");
  histogram_2D->SetYTitle("EMsum (fC)"); 
  gStyle->SetPalette(1);
  gStyle->SetOptLogz();
  histogram_2D->Draw("colz");
  delete c2; // fixes mem leak
