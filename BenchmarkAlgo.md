# AlgorithmBenchmarker
Sorting algorithm benchmarker

package com.myapp.BenchmarkAlgo;
import java.util.*;

public class BenchmarkAlgo {

	public static void main(String[] args) {
		
			int[] array = null;
			Scanner scan = new Scanner(System.in);
			System.out.println("Enter the size of array...!!");
			int size = 0;
			try{
			size = scan.nextInt();
			} catch(InputMismatchException ex){
				System.out.println("Please enter the valid input number");
				scan.close();
				System.exit(0);
			}
			
			System.out.println("Choose senerio");
			System.out.println("1. Best Case senerio");
			System.out.println("2. Average case senerio");
			System.out.println("3. Worst Case senerio");
			
			int choice = 0;
			try{
			choice = scan.nextInt();
			} catch(InputMismatchException ex){
				System.out.println("Please enter the valid input number");
				System.exit(0);
			}
			
			switch(choice){
				case 1:
				array = SortingAlgo.bestCase(size);
				System.out.println("Array of size :" +size + " for Best Case is generated ");
				break;
				
				case 2:
				array = SortingAlgo.averageCase(size);
				System.out.println("Array of size :" +size +" for Average Case is generated ");
				break;
				
				case 3:
				array = SortingAlgo.worstCase(size);
				System.out.println("Array of size :" +size+ " for Worst Case is generated ");
				break;
				
				default :
				System.out.println(" Please enter a valid input...!!");
				return;
			}
			
			System.out.println("Choose sort algo");
			System.out.println("1. Bubble Sort Algorithm");
			System.out.println("2. Selection Sort Algorithm");
			System.out.println("3. Insertion Sort Algorithm");
			System.out.println("4. Merge Sort Algorithm");
			System.out.println("5. Quick Sort Algorithm");
			System.out.println("6. BenchmarkAll");
			
			int algoChoice = 0;
			try{
			algoChoice = scan.nextInt();
			} catch(InputMismatchException ex){
				System.out.println("Please enter the valid input number");
				System.exit(0);
			}
			
			int[] clone = null;
			switch(algoChoice){
				
				case 1:
				clone = SortingAlgo.cloneArray(array);
				SortingAlgo.BubbleSort(clone);
				break;
				
				case 2:
				clone = SortingAlgo.cloneArray(array);
				SortingAlgo.selectionAlgo(clone);
				break;
				
				case 3:
				clone = SortingAlgo.cloneArray(array);
				SortingAlgo.insertionSort(clone);
				break;
				
				case 4:
				clone = SortingAlgo.cloneArray(array);
				SortingAlgo.mergeSort(clone);
				break;
				
				case 5:
				clone = SortingAlgo.cloneArray(array);
				SortingAlgo.quickSortTime(clone,0, clone.length-1);
				break;
			
				case 6:
				clone = SortingAlgo.cloneArray(array);
				SortingAlgo.BubbleSort(clone);
				SortingAlgo.selectionAlgo(clone);
				SortingAlgo.insertionSort(clone);
				SortingAlgo.mergeSort(clone);
				SortingAlgo.quickSortTime(clone, 0, clone.length-1);
				break;
				
				default:
				System.out.println(" enter valid input..!!");
				break;
			}
			}
	}
